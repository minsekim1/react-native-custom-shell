react-native-custom-shell
# 사용자 맞춤으로 만든 쉘 스크립트 파일 모음입니다.
# 리액트 네이티브 새 프로젝트 생성
```
sh starter.sh
```

### sh starter.sh 내용
```
ROOT=~/Desktop
AppName=myNewApp
MacName=mac
cd ~/Desktop &&
git clone https://github.com/Mins97/react_native_mac_starter.git starter &&
cd ~/Desktop/starter &&
cd $ROOT &&
react-native init $AppName --version react-native@0.60.0 &&
cd $ROOT/$AppName/android &&
echo sdk.dir = /Users/$MacName/Library/Android/sdk > local.properties &&
cd .. &&
export ANDROID_SDK=/Users/$MacName/Library/Android/sdk &&
echo 'export PATH=/Users/$MacName/Library/Android/sdk/platform-tools:/Users/mac/.nvm/versions/node/v12.13.0/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/mac/.nvm/versions/node/v12.13.0/bin:/Users/mac/.rvm/bin' >>~/.bash_profile &&
source ~/.bash_profile
```