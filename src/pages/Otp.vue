<template>
    <main class="maincontainer">
        <div class="container">
      <header>
        <i class="fa-solid fa-shield"></i>
      </header>
      <h4> OTP Verification</h4>
      <p>We have send an OTP to your'e Email</p>
      <span>batahemphrey@gmail.com</span>
      <form action="#">
        <div class="input-field">
          <input type="number" placeholder="*"  />
          <input type="number" disabled placeholder="*" />
          <input type="number" disabled placeholder="*"  />
          <input type="number" disabled placeholder="*"  />
        </div>
        <button class="btn">Verify OTP <i class="fa-solid fa-angle-right"></i></button>
      </form>
    </div>
    </main>

</template>

<script>
export default {
  name: 'UserApplications',
}
</script>

<style scoped>
.maincontainer{
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #8aa6f51e;
}
:where(.container, form, .input-field, header) {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.container {
  background: #fff;
  padding: 30px 65px;
  border-radius: 12px;
  row-gap: 20px;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
}
.container header {
  height: 65px;
  width: 65px;
  background: #4070f4;
  color: #fff;
  font-size: 2.5rem;
  border-radius: 50%;
}
.container h4 {
  font-size: 1.25rem;
  color: #333;
  font-weight: 500;
}
form .input-field {
  flex-direction: row;
  column-gap: 10px;
}
.input-field input {
  height: 45px;
  width: 42px;
  border-radius: 6px;
  outline: none;
  font-size: 1.125rem;
  text-align: center;
  border: 1px solid #ddd;
}
.input-field input:focus {
  box-shadow: 0 1px 0 rgba(0, 0, 0, 0.1);
}
.input-field input::-webkit-inner-spin-button,
.input-field input::-webkit-outer-spin-button {
  display: none;
}
form button {
  margin-top: 25px;
  width: 100%;
  color: #fff;
  font-size: 1rem;
  border: none;
  padding: 9px 0;
  cursor: pointer;
  border-radius: 6px;
  pointer-events: none;
  background: #6e93f7;
  transition: all 0.2s ease;
}
.btn.active {
  background: #4070f4;
  cursor: pointer;
}
.btn:hover {
  background: #0e4bf1;
  cursor: pointer;
}

span {
  color:gray;
}
</style>