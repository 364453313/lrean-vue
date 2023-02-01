<template>
    <div class="container">
        <form class="login-form" action="#">
            <h1>登录</h1>
            <input type="text" name="username" placeholder="用户名" />
            <input type="password" name="password" placeholder="密码" />
            <button>登录</button>
        </form>
    </div>
</template>

<script>
export default {
    name: "Login",
};
</script>
<style lang="css" scoped>
.container {
    width: 100vw;
    height: 100vh;
    background: url("./images/bg.png") fixed no-repeat;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
}

.login-form {
    width: 250px;
    height: 280px;
    display: flex;
    flex-direction: column;
    padding: 35px;
    text-align: center;
    position: relative;
    z-index: 100;
    background: inherit;
    border-radius: 18px;
    overflow: hidden;
}

.login-form::before {
    content: "";
    width: calc(100% + 20px);
    height: calc(100% + 20px);
    position: absolute;
    top: -10px;
    left: -10px;
    overflow: hidden;
    background: inherit;
    box-shadow: inset 0 0 0 200px rgba(255, 255, 255, 0.3);
    filter: blur(5px);
    z-index: -1;
}

.login-form h1 {
    font-size: 24px;
    font-weight: 300;
    color: #3d5245;
    margin-bottom: 25px;
}

.login-form input,
.login-form button {
    padding: 0 14px;
    margin: 6px 0;
    height: 36px;
    border: none;
    border-radius: 4px;
    color: #3d5245;
    background-color: rgba(255, 255, 255, 0.6);
}

.login-form input::placeholder {
    color: #3d5245;
}

.login-form button:focus,
.login-form button:focus {
    outline: 0;
}

.login-form button {
    margin-top: 28px;
    background-color: rgba(184, 159, 23, 0.4);
    color: #fff;
    position: relative;
    overflow: hidden;
    transition: 0.4s;
}

.login-form button.enroll {
    background-color: rgba(43, 38, 11, 0.4);
    margin-top: 8px;
}

.login-form button:hover {
    background-color: rgba(209, 179, 9, 0.7);
}

.login-form button::before,
.login-form button::after {
    content: "";
    display: block;
    width: 80px;
    height: 100%;
    background-color: rgba(179, 255, 210, 0.3);
    opacity: 0.5;
    position: absolute;
    top: 0;
    left: 0;
    transform: skew(-15deg);
    filter: blur(30px);
    overflow: hidden;
    transform: translateX(-100px);
}

.login-form button:hover::after {
    width: 40px;
    background: rgba(179, 255, 210, 0.3);
    left: 60px;
    opacity: 0;
    filter: blur(5px);
}

.login-form button:hover::before {
    transition: 1s;
    transform: translateX(320px);
    opacity: 0.7;
}

.login-form button:hover::after {
    transition: 1s;
    transform: translateX(320px);
    opacity: 1;
}
</style>

