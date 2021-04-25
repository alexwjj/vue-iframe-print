# vue-iframe-print

基于 iframe 打印的小工具

## 安装

```bash
npm install vue-iframe-print --save
```

```javascript
import Print from 'vue-iframe-print'

Vue.use(Print);
```
## 示例

[在线打印示例](https://alexwjj.github.io/vue-iframe-print)

你也可以克隆下来本地跑一下

如果你需要扩展功能，可以联系我，或者自己本项目的源文件进行更改

## 使用姿势

#### 打印整页

```
<button v-print>打印整页</button>
```


#### 局部打印:

HTML:
```
<div id="printDiv">
    且随疾风前行，身后亦需流心
</div>

<button v-print="'#printDiv'">只打印指定 DOM</button>
```

#### 局部打印扩展
HTML:
```
<div id="printDiv">
    且随疾风前行，身后亦需流心
</div>

<button v-print="printObj">只打印指定 DOM</button>
```
Vue JavaScript:
```
export default {
    data() {
        return {
            printObj: {
              id: "printDiv",
              popTitle: 'vue-iframe-print',
              extraCss: 'https://www.baidu.com/,https://www.baidu.com/',
              extraHead: '<meta http-equiv="Content-Language"content="zh-cn"/>'
            }
        };
    }
}
```

### API
* `id`:  打印的 ID
* `standard`: 文档类型, 默认html5, 可选 `html5`, `loose`, `strict`
* `extraHead`: 扩展头部
* `extraCss`:  扩展 css
* `popTitle`:  标题
* `endCallback()`: 打印成功后回调
## License

[MIT](http://opensource.org/licenses/MIT)
