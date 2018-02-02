# TouchableOpacity
React Natvie 當中拿來當作按鈕的元件


## Button
- 0.38 版才開始支援
- 只支援最低限度的客製化
  - title
  - color
- iOS、Android 樣式不一樣

![](https://facebook.github.io/react-native/img/buttonExample.png)

使用範例:
```
<Button
  onPress={() => {}}
  title="Hello"
  color="#841584"
/>
```
##  Touchable
- TouchableHighlight
  - 點擊後反黑
- TouchableNativeFeedback
  - Android 會有 Material 效果
- TouchableOpacity
  - 點擊後變透明

點擊範圍
```
hitSlop = {
  top: 0,
  left: 100,
  bottom: 0,
  right: 100
}
```