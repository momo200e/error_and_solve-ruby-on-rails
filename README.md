# 錯誤及解決 #Ruby on Rails
**小筆記，過程中遇到的瓶頸及解決**

## 網頁執行錯誤 ExecJS::ProgramError
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
## bundle install顯示「系統找不到指定的路徑」
![image](https://github.com/momo200e/error_and_solve-ruby-on-rails/blob/master/errror2.jpg)

有人跟我一樣，windows安裝好railsinstall，都會有**找不到路徑**的問題?
```rb
rails-v #系統找不到指定的路徑
bundle install #系統找不到指定的路徑
```
一開始覺得奇怪，
對照了`bin/`中的`rails.bat`和`bundle.bat`之後，

結果發現裡面 _指定的路徑**不一樣**_ 
### rails.bat
![image](https://github.com/momo200e/error_and_solve-ruby-on-rails/blob/master/errror3.jpg)
### bundel.bat
![image](https://github.com/momo200e/error_and_solve-ruby-on-rails/blob/master/errror4.jpg)

`bundel.bat`的路徑完全不存在!!!!!     
**所以把路徑改隊就解決了~~~~ ^^**        
*其他路徑找不到也是一樣
