# Image
用於顯示圖片的 React Component
  - 本地圖片
  - 專案圖片資源 例: `/android/app/src/main/res`
  - 網路圖片
  -

## 本地圖片
```
assets
├── man@2x.png
├── man@3x.png
└── man.png
```
- 圖片有 `@2x`、`@3x` 後輟，React Native 會根據螢幕解析度選擇最適合的大小
- iOS、Android 可以使用相同的路徑
- 只有有用到的圖片會被打包
- 不需要額外設定圖片寬高

使用範例:
```
<Image source={require('./assets/man.png')} />
```
##  App 圖片資源
- Xcode的asset、Android的drawable
- 需要手動設定圖片寬高
- iOS、Android 用法不同
- 注意此時只使用檔案名稱，不帶路徑、後輟

使用範例:
```
<Image source={{uri: 'app_icon'}} style={{width: 40, height: 40}} />

Android:
<Image source={{uri: 'asset:/app_icon.png'}} style={{width: 40, height: 40}} />
```

## 網路圖片

使用範例:
- 需要手動設定圖片寬高

```
<Image
  style={{ height: 34, width: 91, marginBottom: 20 }}
  source={{ uri: 'https://hellojs.school/imgs/hellojs-logo.png' }}
/>
```

```
import React, { Component } from 'react';
import {
  StyleSheet,
  View,
  Image
} from 'react-native';

export default class ImageSample extends Component {
  render() {
    return (
      <View style={styles.container}>
        <Image
          style={{ height: 34, width: 91, marginBottom: 20 }}
          source={{ uri: 'https://hellojs.school/imgs/hellojs-logo.png' }}
        />
        <Image
          style={{ marginBottom: 20 }}
          source={require('./assets/man.png')}
        />
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
    padding: 30,
  },
})
```

## 延伸閱讀
[Images Guide](https://facebook.github.io/react-native/docs/images.html)
