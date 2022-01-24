# <img src='Sources/res/mipmap/icon.png' width='30'> imgui-android

<img src='https://user-images.githubusercontent.com/38132413/150869964-faddb8d9-74e3-4856-ae92-37f8c405c879.jpg' width='600'>

## prerequisites

    sudo apt install -y openjdk-11-jdk-headless adb unzip zip

## NDK (WSL)

    mkdir ~/android-sdk
    export ANDROID_HOME=~/android-sdk
    printf "\nexport ANDROID_HOME=~/android-sdk\n" >> ~/.bashrc

    cd ~/android-sdk
    wget https://dl.google.com/android/repository/commandlinetools-linux-7583922_latest.zip
    unzip commandlinetools-linux-7583922_latest.zip

    yes | $ANDROID_HOME/cmdline-tools/bin/sdkmanager --sdk_root=${ANDROID_HOME} --licenses
    $ANDROID_HOME/cmdline-tools/bin/sdkmanager --sdk_root=${ANDROID_HOME} "build-tools;30.0.2" "cmake;3.10.2.4988404" "ndk;21.3.6528147" "patcher;v4" "platform-tools" "platforms;android-29" "tools"

    mkdir -p $ANDROID_HOME/windows
    cd $ANDROID_HOME/windows
    wget https://dl.google.com/android/repository/platform-tools_r24.0.4-windows.zip
    unzip platform-tools_r24.0.4-windows.zip
    export ADB=$ANDROID_HOME/windows/platform-tools/adb.exe
    printf "\nexport ADB=$ANDROID_HOME/windows/platform-tools/adb.exe\n" >> ~/.bashrc

    # done

## Run

    make keystore
    make run

## Thank

[Dear ImGui](https://github.com/ocornut/imgui)  
[rawdrawandroid](https://github.com/cnlohr/rawdrawandroid)  
