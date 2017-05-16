# 錯誤及解決 #Ruby on Rails
**小筆記，過程中遇到的瓶頸及解決**

![image](https://github.com/momo200e/error_and_solve-ruby-on-rails/blob/master/errror.png)

在windows上運行的是coffee-script-source 1.9.0的問題。

必須將它添加到你的gemfile中：

#### Step1.
```rb
gem 'coffee-script-source', '1.8.0'
```

#### Step2.
```rb
bundle update coffee-script-source
```
