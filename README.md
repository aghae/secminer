# Secure Adminer 
#### Nodejs Secure Wrapper for php Adminer (GUI database Manager Specialy MySQL)

**Install:**

```
Extract & cd to extracted folder 

$ npm install
$ npm start

```

It run on port 8443 by default .you can change port like this :
```
$ port=8000 npm start
```

by default it uses certificate in ssl folder but 
you can generate your certifficate :
```
 $ ./keygen.sh
 $ npm start
```

**Config:**

to enable login for password-less databases like sqlite goto miner/config.php and change  $config_login_password_less value:
```
<?php
$CONFIG_LOGIN_PASSWORD_LESS ='123qwe'

```

to enable otp (one time password) login  in miner/config.php:
```
$CONFIG_LOGIN_OTP = array(
    "enable"        => true , 
    "secret_code"   => "3ekrEtKii"
    /*
        generate new sekret key (change AppName,AppInfo and SecretCode) : 
            https://www.authenticatorApi.com/pair.aspx?AppName=seminer&AppInfo=root&SecretCode=3ekrEtKii
        and scan it with google authenticator :
             https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en&gl=US
    */
);

```


good luck ;)
