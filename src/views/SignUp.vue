<template>
    <html>
        <body>
            <div id="login-box">
                <div class="left">
                    <h1>Sign up</h1>
                    <form method="POST" action="{{ route('register') }}">
                        <input
                            id="name"
                            type="text"
                            placeholder="Username"
                            class="form-control @error('name') is-invalid @enderror"
                            name="name"
                            required
                            autocomplete="name"
                            autofocus
                        />

                        <span class="invalid-feedback" role="alert">
                            <strong>{{ $message }}</strong>
                        </span>

                        <input
                            id="email"
                            type="email"
                            placeholder="E-mail"
                            class="form-control @error('email') is-invalid @enderror"
                            name="email"
                            required
                            autocomplete="email"
                        />

                        <span class="invalid-feedback" role="alert">
                            <strong>{{ $message }}</strong>
                        </span>
                        <input
                            id="password"
                            type="password"
                            placeholder="Password"
                            class="form-control @error('password') is-invalid @enderror"
                            name="password"
                            required
                            autocomplete="new-password"
                        />

                        <span class="invalid-feedback" role="alert">
                            <strong>{{ $message }}</strong>
                        </span>

                        <input
                            id="password-confirm"
                            type="password"
                            placeholder="Retype password"
                            class="form-control"
                            name="password_confirmation"
                            required
                            autocomplete="new-password"
                        />

                        <input type="submit" name="signup_submit" />
                    </form>
                </div>

                <div class="right">
                    <span class="loginwith"
                        >Sign in with<br />
                        <p>social network</p></span
                    >

                    <button class="social-signin facebook">
                        Log in with facebook
                    </button>
                    <button class="social-signin twitter">
                        Log in with Twitter
                    </button>
                    <button class="social-signin google">
                        Log in with Google+
                    </button>
                </div>
                <div class="or">OR</div>
            </div>
        </body>
    </html>
</template>

<script>
// @ is an alias to /src

export default {
    name: "SignUp",
};
</script>
<style>
@import url(https://fonts.googleapis.com/css?family=Roboto:400,300,500);
*:focus {
    outline: none;
}

body {
    margin: 0;
    padding: 0;
    background: #ddd;
    font-size: 16px;
    color: #222;
    font-family: "Roboto", sans-serif;
    font-weight: 300;
}

#login-box {
    position: relative;
    margin: 5% auto;
    width: 600px;
    height: 400px;
    background: #fff;
    border-radius: 2px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
}

.left {
    position: absolute;
    top: 0;
    left: 0;
    box-sizing: border-box;
    padding: 40px;
    width: 300px;
    height: 400px;
}

h1 {
    margin: 0 0 20px 0;
    font-weight: 300;
    font-size: 28px;
}

input[type="text"],
input[type="password"] {
    display: block;
    box-sizing: border-box;
    margin-bottom: 20px;
    padding: 4px;
    width: 220px;
    height: 32px;
    border: none;
    border-bottom: 1px solid #aaa;
    font-family: "Roboto", sans-serif;
    font-weight: 400;
    font-size: 15px;
    transition: 0.2s ease;
}
div span p {
    color: black;
}
input[type="text"]:focus,
input[type="password"]:focus {
    border-bottom: 2px solid #16a085;
    color: #16a085;
    transition: 0.2s ease;
}

input[type="submit"] {
    margin-top: 28px;
    width: 120px;
    height: 32px;
    background: #16a085;
    border: none;
    border-radius: 2px;
    color: #fff;
    font-family: "Roboto", sans-serif;
    font-weight: 500;
    text-transform: uppercase;
    transition: 0.1s ease;
    cursor: pointer;
}

input[type="submit"]:hover,
input[type="submit"]:focus {
    opacity: 0.8;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
    transition: 0.1s ease;
}

input[type="submit"]:active {
    opacity: 1;
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.4);
    transition: 0.1s ease;
}

.or {
    position: absolute;
    top: 180px;
    left: 280px;
    width: 40px;
    height: 40px;
    background: #ddd;
    border-radius: 50%;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
    line-height: 40px;
    text-align: center;
}

.right {
    position: absolute;
    top: 0;
    right: 0;
    box-sizing: border-box;
    padding: 40px;
    width: 300px;
    height: 400px;
    background: url("https://goo.gl/YbktSj");
    background-size: cover;
    background-position: center;
    border-radius: 0 2px 2px 0;
}

.right .loginwith {
    display: block;
    margin-bottom: 40px;
    font-size: 28px;
    color: #fff;
    text-align: center;
}

button.social-signin {
    margin-bottom: 20px;
    width: 220px;
    height: 36px;
    border: none;
    border-radius: 2px;
    color: #fff;
    font-family: "Roboto", sans-serif;
    font-weight: 500;
    transition: 0.2s ease;
    cursor: pointer;
}

button.social-signin:hover,
button.social-signin:focus {
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
    transition: 0.2s ease;
}

button.social-signin:active {
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.4);
    transition: 0.2s ease;
}

button.social-signin.facebook {
    background: #32508e;
}

button.social-signin.twitter {
    background: #55acee;
}

button.social-signin.google {
    background: #dd4b39;
}
#email {
    display: block;
    box-sizing: border-box;
    margin-bottom: 20px;
    padding: 4px;
    width: 220px;
    height: 32px;
    border: none;
    border-bottom: 1px solid #aaa;
    font-family: "Roboto", sans-serif;
    font-weight: 400;
    font-size: 15px;
    transition: 0.2s ease;
}
</style>
