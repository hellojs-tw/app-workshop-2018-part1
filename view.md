# View
建構 UI 的基礎元件，支持 [Flexbox](https://facebook.github.io/react-native/docs/flexbox.html) 佈局、[Style](https://facebook.github.io/react-native/docs/style.html)、一些觸摸處理、和一些無障礙功能的容器，並且它可以放到其它的視圖裡，也可以有任意多個任意類型的子視圖。不論在什麼平台上，View都會直接對應一個平台的原生視圖，無論它是 UIView、<div> 還是 android.view 等等


常用 style:
```
backgroundColor: 背景顏色
flex: 排版方式
weight: 寬度
margin: 邊界
padding: 留白、內距
borderRadius: 圓弧
borderColor: 邊框顏色
borderWidth: 邊框寬度
```

特殊 props: 
```
elevation 使用Android原生的 elevation API來設置 View 的高度產生陰影的效果
```

```
import React, { Component } from 'react';
import {
  View,
} from 'react-native';

export default class ViewSample extends Component {
  render() {
    return (
      <View style={{ flex: 1 }}>
       <View style={{backgroundColor: 'red', flex: 1}} />
       <View style={{backgroundColor: 'blue', flex: 1}} />
        <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center', }}>
          <View elevation={10} style={{ height: 100, width: 100, backgroundColor: '#eee', justifyContent: 'center' alignItems: 'center' }}>
            <Text>123</Text>
          </View>
        </View>
      </View>
    );
  }
}
```
