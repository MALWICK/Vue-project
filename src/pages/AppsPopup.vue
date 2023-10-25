<template>
    <div class="overlay">
        <div class="popup">
          <button @click="openModal()" class="close">X</button>
          <div class="header">
            <h2>This App will be added to your List of Installed Apps</h2>
          </div>
          <div class="innercont">
            <div class="smallheader">
              <h3>
                <span class="attention">First! </span> Provide your User Inforamtion for this
                Platform
              </h3>
            </div>

            <form>
              <div class="first__row">
                <div class="left__cont">
                  <span class="label">First Name</span>
                  <div class="input__holder">
                    <input
                      type="text"
                      class="first__name"
                      placeholder="Enter your first name"
                      value="Bata"
                    />
                  </div>
                </div>
                <div class="right__cont">
                  <span class="label">Last Name</span>
                  <div class="input__holder">
                    <input
                      type="text"
                      class="first__name"
                      placeholder="Enter your last Name"
                      value="Humphrey"
                    />
                  </div>
                </div>
              </div>
              <div class="fullrow">
                <div class="full__cont">
                  <span class="label">Email Address</span>
                  <div class="fullinput__holder">
                    <input
                      type="email"
                      class="first__name"
                      placeholder="Enter your first name"
                      value="BataHumphrey@gmail.com"
                    />
                  </div>
                </div>
                <div class="apikey__cont">
                  <p class="api__key">
                    <span class="apispan">ApiKey:</span> Mh&resa18903679800387845*****
                  </p>
                  <button class="copy">Copy <i class="fa-solid fa-copy"></i></button>
                </div>
                <div class="confirm">
                  <button @click="openModal()" >Confirm</button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
</template>

<script>
export default {
props:["openModal"]
}
</script>

<style scope>

.overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.7);
 
 
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
/* .overlay:target {
  visibility: visible;
  opacity: 1;
} */

.popup {
  width: 40.0625vw;
  height: 47.98360655737705vh;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
  border-radius: 0.8rem;
  display: flex;
  position:relative;
  flex-direction: column;
  padding: 4px 12px 2px;
  background: white;
}

.close {
   position: absolute;
  top: -8px;
  right: -12px;
  height: 55px;
  width: 55px;
  outline:none;
  border:none;
  border-radius:50%;
  background: white;
  box-shadow: rgba(61, 61, 63, 0.2) 0px 7px 29px 0px;
  cursor:pointer;
}

.close:hover {
  background: black;
  color: #fff;
  
}

.innercont {
  width: 98%;
  height: 100%;
  padding: 5px 5px;
  /*  background-color: red; */
}

.header {
  width: 100%;
  font-family: sans-serif;
  font-weight: 700;
  font-size: 18px;
  border-bottom: 1px solid lightgray;
}

.first__row {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 16px;
  padding: 3px 5px;
  margin-top: 3px;
  /* background-color: green; */
}

.fullrow {
  width: 100%;
  padding: 3px 5px;
/*   background: rgb(0, 124, 128); */
}

.full__cont {
  width: 100%;
  margin-top: 2px;
 /*  background: green; */
}

.fullinput__holder {
  width: 100%;
  margin-top: 10px;
}

.fullinput__holder input {
  min-width: 95%;

  /*  border-radius: 0.6rem; */
  outline: none;
  margin: 0;
  font-variant: tabular-nums;
  list-style: none;
  font-feature-settings: 'tnum', 'tnum';
  position: relative;
  display: inline-block;

  padding: 8px 11px;
  color: rgba(0, 0, 0, 0.85);
  font-size: 14px;
  line-height: 1.5715;
  background-color: #fff;
  background-image: none;
  border: 1px solid #d9d9d9;
  border-radius: 8px;
  transition: all 0.3s;
}

.left__cont {
  width: 49%;
}

.label {
  font-size: 18px;
  font-weight: 700;
  line-height: 25px;
}

.right__cont {
  width: 49%;
}

.input__holder {
  width: 100%;
  margin-top: 10px;
}

.input__holder input {
  min-width: 90%;
  padding: 14px;

  outline: none;
  margin: 0;
  font-variant: tabular-nums;
  list-style: none;
  font-feature-settings: 'tnum', 'tnum';
  position: relative;
  display: inline-block;

  padding: 8px 11px;
  color: rgba(0, 0, 0, 0.85);
  font-size: 14px;
  line-height: 1.5715;
  background-color: #fff;
  background-image: none;
  border: 1px solid #d9d9d9;
  border-radius: 8px;
  transition: all 0.3s;
}

input:hover {
  border: 1px solid #007fff;
  border-color: 1px solid #007fff;
}

input[type='text']:focus {
  border: 1px solid #007fff;
}

.apikey__cont {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-left: 10px;
  padding-right: 10px;
  margin-top: 10px;
}

.copy {
  margin-right: 23px;
  border-radius: 8px;
  border-style: none;
  box-sizing: border-box;
  color: #ffffff;
  cursor: pointer;
  display: inline-block;
  font-family: 'Haas Grot Text R Web', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-size: 14px;
  font-weight: 500;
  height: 40px;
  line-height: 20px;
  list-style: none;
  outline: none;
  padding: 10px 16px;
  position: relative;
  text-align: center;
  text-decoration: none;
  transition: color 100ms;
  vertical-align: baseline;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  background: #2d2f3157;
}

.copy:hover,
.copy:focus {
  background-color: black;
}

.attention {
  font-size: 24px;
  font-weight: 700;
  color: #007fff;
}

.confirm {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 9px;
}

.confirm button {
  border-radius: 8px;
  border-style: none;
  box-sizing: border-box;
  color: #ffffff;
  cursor: pointer;
  display: inline-block;
  font-family: 'Haas Grot Text R Web', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-size: 18px;
  font-weight: 700;
  height: 40px;
  width: 97%;
  line-height: 20px;
  list-style: none;
  outline: none;
  padding: 10px 16px;
  position: relative;
  text-align: center;
  text-decoration: none;
  transition: color 100ms;
  vertical-align: baseline;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  background: #0080ffc7;
}

.confirm button:hover {
  background: black;
}

.smallheader {
  width:100%;
  display: flex;
  align-items: center;
  justify-content:center;
}
</style>