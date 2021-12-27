nodejs 14.17.0

yarn install
npx pod-install


## 환경변수 설정법
https://velog.io/@heumheum2/React-Native-Multiple-Environments

## 파이어베이스 설정법
https://rnfirebase.io

## fcm 이용해서 ios 푸시알림 
https://velog.io/@mayinjanuary/React-Native-Firebase-로-푸쉬-알림-구현하기-2-IOS-앱-세팅하기

## 리액트 네이티브 벡터아이콘즈 설정법
https://dev-yakuza.posstree.com/ko/react-native/react-native-vector-icons/

## App.js 에서 navigation 사용하는 법
https://reactnavigation.org/docs/navigating-without-navigation-prop/
https://velog.io/@mayinjanuary/React-Native-navigation-without-navigation-prop

## splash screen 설정
https://velog.io/@hojin9622/React-Native-Splash-Screen-제작IOS


## 다크 모드 disable 설정
ios 의 경우 AppDelegate.m 의 didFinishLaunchingWithOptions 안에다가 아래 항목 추가

`if (@available(iOS 13.0, *)) { rootView.overrideUserInterfaceStyle = UIUserInterfaceStyleLight; }`

참고로 rootView 가 정의된곳 아래에다가 집어넣어야 한다.

안드로이드의 경우 styles.xml 을 다음과 같이 작성
```
<resources>

    <!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.NoActionBar">
        <!-- Customize your theme here. -->
        <item name="android:textColor">#000000</item>
        <item name="android:forceDarkAllowed">false</item>
        
    </style>

</resources>
```
디폴트 값이 AppCompat.DayNight 일텐데 이걸 AppCompat.Light 로 바꿔주고 forceDarkAlloed 항목을 false 로 추가하면 된다.


## app name 변경

- app.json 의 displayName 수정
- ios : xCode에서 General탭 > Identity > Display Name을 바꿔주면 됩니당
- android : android/app/src/main/res/values/strings.xml 코드를 수정.
app_name 변수를 수동으로 변경. 변경하고 다시 코드 실행하면 앱이름 바뀜.
```
<resources>
	<string name="app_name">새로운 앱 이름</string>
</resources>
```