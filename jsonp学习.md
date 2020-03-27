## jsonp原理介绍

- jsonp就是为了解决前端的跨域问题而进行的一项设计，jsonp之所以能实现跨域，是因为`它发送的不是ajax请求`，它`动态创建了script标签`，script标签是不受同源策略限制的，将script的src指向正式的服务器地址。

## Vue中jsonp插件使用

- [Github地址](https://github.com/webmodules/jsonp)

### 安装

```shell
npm install jsonp --save-dev
```

### 引入jsonp

```typescript
import jsonp from 'jsonp';
```

### 请求数据

```javascript
jsonp(
        'url?callback',
        (err, data) => {
          // console.log(data.data);
          const list = data.data.list.map(item => {
            return {
              name: item.name,
              value: item.value
            };
          });
          // console.log(list);
          // 将数据给到地图
          option.series[0].data = list;
          // console.log(option.series[0].map);
          // 在mounted加载设置
          this.mycharts.setOption(option);
        }
      );
```

