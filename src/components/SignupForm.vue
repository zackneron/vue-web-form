<template>
  <form>
      <label>Email:</label>
      <input type="email" required v-model='email'>
      <label>Password:</label>
      <input type="password" required v-model='password'>

      <label>Role:</label>
      <select v-model="role">
          <option value="select">Select</option>
          <option value="developer">Web Developer</option>
          <option value="designer">Web Designer</option>
      </select>

      <div class="terms">
          <input type="checkbox" v-model="terms">
          <label>Accept terms and condition</label>
      </div>

      <div class="names">
          <div>
              <input type="checkbox" value="Zack" v-model="names">
              <label>Zack</label> 
          </div>
          <div>
              <input type="checkbox" value="Neron" v-model="names">
              <label>Neron</label> 
          </div>
          <div>
              <input type="checkbox" value="Mutombo" v-model="names">
              <label>Mutombo</label> 
          </div>
          <div>
              <input type="checkbox" value="Katshi" v-model="names">
              <label>Katshi</label> 
          </div>
      </div>
  </form>
  <p>Email: {{password}}</p>
  <p>Password: {{password}}</p>
  <p>Role: {{role}}</p>
  <p>Terms accepted: {{terms}}</p>
  <p>Names: {{ names}}</p>
</template>

<script>
export default {
    data(){
        return {
            email: '',
            password: '',
            role: 'select',
            terms: false,
            names: []
        }
    }
}
</script>

<style>
form {
    max-width: 420px;
    margin: 30px auto;
    background-color: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    text-transform: uppercase;
    font-weight: bold;
}
input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}

input[type="checkbox"]{
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
}

.names > div {
    background-color: rgb(243, 243, 243);
    padding: 15px;
    border-radius: 5px;
    margin-bottom: 10px;
}
.names label {
    margin: 0;
}
</style>