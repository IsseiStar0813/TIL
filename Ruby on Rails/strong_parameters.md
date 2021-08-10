# Strong ParametersはDBに入れる値を制限することで、不正なパラメータの入力を防ぐ仕組み
* requireでPOSTで受け取る値のキーを設定
* permitで許可するカラムを設定
```
params.require(:user).permit(:name, :email, :password, password_confirmation)
```
permit に　password_confirmationを含まないと、has_secure_passwordがうまく動作しない
