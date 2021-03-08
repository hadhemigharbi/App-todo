<template>

  <form
    class="rounded mx-auto max-w-3xl w-full my-6 inputs space-y-4 bg-center"
  >
  <div id="app" class="">
    <div class="flex flex-nowrap">
      <div class="card mr-8">
        <div class="flex space-x-4">
          <div class="w-1/2">
            <label for="firstname" class="font-black">First Name</label>
            <div>
              <input
                class="border border-gray-400 px-4 py-2 rounded w-full focus:outline-none focus:ring focus:border-blue-300"
                type="text"
                name="firstname"
                id="firstname"
                maxlength="200"
                minlength="20"
                v-model="firstname"
                onkeypress="return ((event.charCode > 64 && event.charCode < 91) || (event.charCode > 96 && event.charCode < 123) || event.charCode == 8 || event.charCode == 32 || (event.charCode >= 48 && event.charCode <= 57));"
                required
              />
            </div>
          </div>

          <div class="w-1/2">
            <label for="lastname" class="font-black">Last Name</label>
            <input
              class="border border-gray-400 px-4 py-2 rounded w-full focus:outline-none focus:ring focus:border-blue-300"
              type="text"
              name="lastname"
              id="lastname"
              maxlength="200"
              minlength="20"
              v-model="lastname"
              onkeypress="return ((event.charCode > 64 && event.charCode < 91) || (event.charCode > 96 && event.charCode < 123) || event.charCode == 8 || event.charCode == 32 || (event.charCode >= 48 && event.charCode <= 57));"
              required
            />
          </div>
        </div>

        <div class="mt-4">
          <label for="address" class="font-black">Current Address</label>
          <input
            class="placeholder-gray-500 placeholder-opacity-100 border border-gray-400 px-4 py-2 rounded w-full focus:outline-none focus:ring focus:border-blue-300"
            type="email"
            name="address"
            id="address"
            placeholder="Example@gmail.com"
            maxlength="200"
            minlength="20"
            v-model="address"
            required
          />
        </div>

        <div class="mt-4">
          <label for="password" class="font-black">Password</label>
          <input
            class="placeholder-gray-500 placeholder-opacity-100 border border-gray-400 px-4 py-2 rounded w-full focus:outline-none focus:ring focus:border-blue-300"
            type="password"
            name="password"
            id="password"
            placeholder="**************"
            maxlength="200"
            minlength="20"
            v-model="password"
            onkeypress="return ((event.charCode > 64 && event.charCode < 91) || (event.charCode > 96 && event.charCode < 123) || event.charCode == 8 || event.charCode == 32 || (event.charCode >= 48 && event.charCode <= 57));"
            required
          />
        </div>

        <div class="mt-4">
          <label for="Conformpassword" class="font-black"
            >Repeat Password</label
          >
          <input
            class="placeholder-gray-500 placeholder-opacity-100 border border-gray-400 px-4 py-2 rounded w-full focus:outline-none focus:ring focus:border-blue-300"
            type="password"
            name="Conformpassword"
            id="Conformpassword"
            placeholder="**************"
            maxlength="200"
            minlength="20"
            v-model="Conformpassword"
            onkeypress="return ((event.charCode > 64 && event.charCode < 91) || (event.charCode > 96 && event.charCode < 123) || event.charCode == 8 || event.charCode == 32 || (event.charCode >= 48 && event.charCode <= 57));"
            required
          />
        </div>

        <div class="mt-4">
          <label for="gender" class="font-black">Gender</label>
          <ul>
            <li>
              <input type="radio" name="gender" id="male" required />
              <label for="male" class="labled">Male</label>
            </li>
            <li>
              <input type="radio" name="gender" id="female" required />
              <label for="female" class="labled">Female</label>
            </li>
          </ul>
        </div>

        <div>
          <input type="checkbox" class="rounded text-pink-500 mt-4" required />
          <label class="font-mono tracking-tighter"
            >&nbsp; I Agree to the terms of users</label
          >
        </div>
        <div>
          <div class="px-4 py-6 flex justify-between">
            <button
              type="reset"
              class="bg-red-900 text-white hover:bg-red-700 px-4 py-2 text-teal-600"
            >
              Remove
            </button>
            <div class="flex space-x-4">
              <button
                type="submit"
                @click="persist"
                class="bg-blue-800 px-4 py-2 text-white transform hover:scale-110 motion-reduce:transform-none"
              >
                Sign Up
              </button>
              <button
                type="menu"
                class="bg-blue-600 px-4 py-2 text-white transform hover:scale-110 motion-reduce:transform-none"
              >
                Edit
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="cardtwo ml-8 bg-center">
        <button
          type="button"
          class="rounded-full py-2 px-12 mx-2 my-4 mt-48 bg-red-400 text-white hover:bg-red-600 font-semibold text-teal-600"
        >
          <div class="flex justify-center space-x-2">
            <div>
              <i class="fab fa-google"></i>
            </div>
            <div>
              <span
                ><a href="https://www.google.com/accounts/Login?hl=fr"
                  >Connect With Google</a
                ></span
              >
            </div>
          </div>
        </button>

        <button
          type="button"
          class="rounded-full py-2 px-12 mx-2 my-4 bg-blue-600 text-white hover:bg-red-700 px-4 py-2 font-semibold text-teal-600"
        >
          <div class="flex justify-center space-x-2">
            <div>
              <i class="fab fa-twitter"></i>
            </div>
            <div>
              <span
                ><a href="https://twitter.com/login?lang=fr"
                  >Connect with Twitter</a
                ></span
              >
            </div>
          </div>
        </button>

        <button
          type="button"
          class="rounded-full py-2 px-12 mx-2 my-4 bg-gray-500 text-white hover:bg-red-700 px-4 py-2 font-semibold text-teal-600"
        >
          <div class="flex justify-center space-x-2">
            <div>
              <i class="fab fa-linkedin-in"></i>
            </div>
            <div>
              <span
                ><a
                  href="https://www.linkedin.com/login/fr?fromSignIn=true&trk=guest_homepage-basic_nav-header-signin"
                  >Connect with LinkdeIn</a
                ></span
              >
            </div>
          </div>
        </button>
      </div>
    </div>
  </div>
  </form>
</template>

<script>
export default {
  el: '#app',
  mounted() {
    if (localStorage.firstname) {
      this.firstname = localStorage.firstname;
    }
    if (localStorage.lastname) {
      this.lastname = localStorage.lastname;
    }
    if (localStorage.address) {
      this.address = localStorage.address;
    }
    if (localStorage.password) {
    this.password = localStorage.password;
    }
    if (localStorage.gender) {
    this.gender = localStorage.gender;
    }
  },
  methods: {
    persist() {
      localStorage.firstname = this.firstname;
      localStorage.lastname = this.lastname;
      localStorage.address = this.address;
      localStorage.password = this.password;
      localStorage.gender = this.gender;
      console.log('maintenant prétendre que j\'ai fait plus de choses...');
    }
  },
};
</script>

<style lang="scss" scoped>
.body-bg {
  background-color: #ac52e7;
  background-image: linear-gradient(315deg, #d382c5 0%, #c9c263 74%);
}
.card {
  background-color: #ac52e7;
  background-image: linear-gradient(315deg, #5035c9 0%, #9c253f 74%);
  display: flex;
  flex-direction: column;
  width: 500px;
  padding: 20px 25px;
  border-radius: 20px;
  box-shadow: 0 19px 38px rgba(0, 0, 0, 0.13);
}

.cardtwo {
  background-color: #ac52e7;
  background-image: linear-gradient(315deg, #5035c9 0%, #9c253f 74%);
  display: flex;
  flex-direction: column;
  width: 500px;
  padding: 10px 15px;
  border-radius: 20px;
  box-shadow: 0 19px 38px rgba(0, 0, 0, 0.13);
}
label {
  color: #c9bbc9;
}
.labled {
  margin-left: 35px;
  color: white;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}
button {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}
input[type="text"] {
  text-transform: capitalize;
}

input[type="radio"] {
  position: absolute;
  width: 20px;
  height: 20px;
}

ul {
  list-style-type: none;
  padding-left: 50px;
  margin: 0;
}

li {
  display: block;
  position: relative;
  padding: 7px 0px;
}
</style>
