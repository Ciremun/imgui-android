# imgui-android

## prerequisites

    sudo apt install -y openjdk-11-jdk-headless adb unzip zip

## NDK

    mkdir ~/android-sdk
    export ANDROID_HOME=~/android-sdk
    printf "\nexport ANDROID_HOME=~/android-sdk\n" >> ~/.bashrc

    cd ~/android-sdk
    wget https://dl.google.com/android/repository/commandlinetools-linux-7583922_latest.zip
    unzip commandlinetools-linux-7583922_latest.zip

    yes | $ANDROID_HOME/cmdline-tools/bin/sdkmanager --sdk_root=${ANDROID_HOME} --licenses
    $ANDROID_HOME/cmdline-tools/bin/sdkmanager --sdk_root=${ANDROID_HOME} "build-tools;30.0.2" "cmake;3.10.2.4988404" "ndk;21.3.6528147" "patcher;v4" "platform-tools" "platforms;android-29" "tools"

    # done

## Run

    make keystore
    make run

## Thank

[Dear ImGui](https://github.com/ocornut/imgui)
[rawdrawandroid](https://github.com/cnlohr/rawdrawandroid)
