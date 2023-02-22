<script>
import AleartPassword from './AleartPassword.vue';
export default {
  data() {
    return {
      email: '',
      password: '',
      password2: '',
      passwordError: false,
    };
  },
  watch: {
    password2() {
      if (this.password2 !== this.password) {
        this.passwordError = true;
      } else {
        this.passwordError = false;
      }
    },

    password(){
      if (this.password.length < 6) {
        this.passwordError = true;
      } else {
        this.passwordError = false;
      }

      if (this.password2 !== this.password) {
        this.passwordError = true;
      } else {
        this.passwordError = false;
      }
    }
  },
  components: {
    AleartPassword,
  },
};
</script>


<template>
  <div class="card w-full max-w-sm shadow-2xl bg-base-100">
    <div class="card-body">
      <div class="form-control">
        <label class="label">
          <span class="label-text">邮箱</span>
        </label>
        <input type="text" placeholder="email" class="input input-bordered" v-model="email" />
      </div>
      <div class="form-control">
        <label class="label">
          <span class="label-text">密码</span>
        </label>
        <input type="text" placeholder="密码最少6位" class="input input-bordered" v-model="password" />
      </div>
      <div class="form-control">
        <label class="label">
          <span class="label-text">确认密码</span>
          <AleartPassword :passwordError="passwordError" />
        </label>
        <input type="text" placeholder="password" class="input input-bordered" v-model="password2" />
        
      </div>

      <div class="form-control mt-3">
        <button class="btn btn-primary" :disabled="passwordError">注册</button>
      </div>
    </div>
  </div>
</template>