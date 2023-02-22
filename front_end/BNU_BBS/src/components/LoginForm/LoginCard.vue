<script>
export default{
  methods: {
    toRegister() {
      this.$router.push('/register');
    },
  },
}
</script>

<template>
  <div class="card flex-shrink-0 w-full max-w-sm shadow-2xl bg-base-100">
    <div class="card-body">
      <div class="form-control">
        <label class="label">
          <span class="label-text">邮箱</span>
        </label>
        <input type="text" placeholder="email" class="input input-bordered" />
      </div>
      <div class="form-control">
        <label class="label">
          <span class="label-text">密码</span>
        </label>
        <input type="text" placeholder="password" class="input input-bordered" />
        <label class="label">
          <a href="#" class="label-text-alt link link-hover">忘记密码?</a>
        </label>
      </div>
      <div class="form-control mt-3">
        <button class="btn btn-primary">登陆</button>
      </div>
      <div class="form-control mt-3">
        <button class="btn btn-primary" @click= "toRegister">还未拥有账号？点击注册。</button>
      </div>
    </div>
  </div>
</template>