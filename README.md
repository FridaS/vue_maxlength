# vue_maxlength
Limit the input byte length of the input box:
- 2 bytes per character in Chinese
- 1 byte per character in English

限制输入框的输入字节长度，其中：
- 一个中文字符占2个字节
- 一个英文字符占1个字节


用法 Usage：
```javascript
import Maxlength from 'vue_input_maxlength'
Vue.use(Maxlength)

// 用法1
<el-input v-model="test" v-maxlength:test="10"></el-input>

// 用法2
/** 
 * 指令参数：
 * @param {Number} limit 限制的字节数
 * @param {String} field 需要改变的组件data中的字段（具体访问路径）
 */
<li v-for="(item, i) in test">
    <el-input v-model="item.a" v-maxlength="{limit:10, field:`test.${i}.a`}"></el-input>
</li>
```