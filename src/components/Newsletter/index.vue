<template>
  <div class="container newsl_container">
      <h2>Join to our newsletter</h2>
      <div class="form">
          <input type="text" v-model="email">
          <button @click="submitHandler">Subscribe</button>
      </div>
      <div class="error_label">
          <div>{{error}}</div>
      </div>
      <div class="success_label">
          <div>{{success}}</div>
      </div>
      <div class="small">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi eum provident quidem iure debitis! Suscipit debitis provident ipsum. Cumque magnam commodi, dolorum quibusdam nostrum officia.</p>
      </div>
  </div>
</template>

<script>
export default {
data(){
    return{
        email:"",
        error:'',
        success:'',
    }
},
methods:{
    validate(email){
        let valid = [true, '']
         let re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
        if(!re.test(email)){
            valid = [false, 'Enter valid email']
        }
        if(email === ''){
            valid = [false, 'Its empty']
        }
        return valid
    },
    submitHandler(){
        let valid = this.validate(this.email)
        if(valid[0]){
            this.error = ''
            this.addEmail(this.email)
        }else{
            this.error = valid[1]
        }
        
    },
    addEmail(email){
        this.$http.get(`users.json?orderBy="email"&&equalTo="${email}"`)
        .then(responce =>{
            if(Object.getOwnPropertyNames(responce.data).length === 0){
                this.$http.post('user.json', {email: this.email})
                .then(() =>{
                    this.success = 'Thank you'
                })
            }else{
                this.success = 'Alredy on the list'
            }
        })
        this.clearSuccess()
    },
    clearSuccess(){
        setTimeout(() =>{
            this.email =''
            this.success =''
        },3000)
    }
}
}
</script>

<style>

</style>