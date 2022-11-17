# Village_Era

Here we have made a Village helping application using java libraries like **Lottie** or **_TensorFlow Lite_**.

<br><img src="app/src/main/res/drawable/villageera.svg" alt="drawing" height="540"/>

It is a *Villager supporting app* where the user will get **_A right for making post regarding the complaints in the village also they can suggest or advice_**.

The *Sarpanch* can view the posts **_also he can make a notice for whole village with in his finger tips_**.

1. You need to install TensorFlow Lite from [here](https://www.tensorflow.org/)

```Java
new Handler().postDelayed(new Runnable() {
	@Override
	public void run() {
	
		onBoardingScreen = getSharedPreferences("onBoardingScreen", MODE_PRIVATE);
                boolean isFirstTime = onBoardingScreen.getBoolean("firstTime", true);

                if (isFirstTime) {

                    SharedPreferences.Editor editor = onBoardingScreen.edit();
                    editor.putBoolean("firstTime", false);
                    editor.commit();

                    startActivity(new Intent(MainActivity.this, OnBoardingScreen.class));
                    finish();
                } else {
                    startActivity(new Intent(MainActivity.this, LoginActivity.class));
                    finish();
		}
	}
}, SPLASH_TIMER);

```

### Important Instructions :

* The user needs to login to utilize the services.

Reference Code : 
```Java
    private void SignIn(String email, String pass) {
        mAuth.signInWithEmailAndPassword(email, pass).addOnCompleteListener(this, new OnCompleteListener<AuthResult>() {
            @Override
            public void onComplete(@NonNull Task<AuthResult> task) {
                if (task.isSuccessful()) {
                    startActivity(new Intent(LoginActivity.this, DashBoardActivity.class));
                    finish();
                } else {
                    Toast.makeText(LoginActivity.this, "Some thing went wrong", Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
```
Reference Images : <br>
	<br><img src="app/src/main/res/drawable-v24/Splash Screen.png" alt="drawing" width="200" height="450"/>
	<img src="app/src/main/res/drawable-v24/Screen 4.png" alt="drawing" width="200" height="450"/>
	<img src="app/src/main/res/drawable-v24/Screen 3.png" alt="drawing" width="200" height="450"/>
	<br><img src="app/src/main/res/drawable-v24/Screen 2.png" alt="drawing" width="200" height="450"/>
	<img src="app/src/main/res/drawable-v24/Screen 1.png" alt="drawing" width="200" height="450"/>
	<img src="app/src/main/res/drawable-v24/Register.png" alt="drawing" width="200" height="450"/>
	
This is the README file for Village Era repository. [^1]

[^1]: By : Village Era.
