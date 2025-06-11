# fast-typed.js

> ⚡️ 本库是基于 [typed.js](https://github.com/mattboldt/typed.js) 的 fork，专为极致字符输出速度和批量输出优化。

## 主要特性

- **一次输出多个字符**：通过 `newCharPerStep` 参数控制每次输出的字符数，极大提升速度上限。
- **typeSpeed=0 真正极速**：当 `typeSpeed` 设为 0 时，字符几乎瞬间输出。
- 完全兼容 typed.js 的全部用法和参数。

---

## 安装与使用

### CDN

```html
<script src="/path/to/fast-typed.js"></script>
<span id="element"></span>
<script>
  var typed = new Typed('#element', {
    strings: ['<i>First</i> sentence.', '& a second sentence.'],
    typeSpeed: 0,
    newCharPerStep: 5, // 每次输出5个字符
  });
</script>
```

### NPM

```bash
npm install fast-typed.js
```

### ESM 用法

```js
import Typed from 'fast-typed.js';
const typed = new Typed('#element', {
  strings: ['<i>First</i> sentence.', '& a second sentence.'],
  typeSpeed: 0,
  newCharPerStep: 10,
});
```

---

## 新增参数

- `newCharPerStep`：每次输出的字符数，默认 1。数值越大，速度越快。

## 主要参数（兼容 typed.js）

- `strings`：要输出的字符串数组
- `typeSpeed`：每个字符输出间隔（毫秒），0 为最快
- `backSpeed`：回退速度
- `startDelay`：开始前延迟
- `backDelay`：回退前延迟
- `loop`：是否循环
- `showCursor`：是否显示光标
- ...（其余参数同 typed.js）

---

## 示例

```js
var typed = new Typed('#element', {
  strings: ['极速输出', '一次输出多个字符！'],
  typeSpeed: 0,
  newCharPerStep: 8,
  loop: true,
});
```

---

## 其它用法与高级功能

- 支持 HTML 字符串、回退、暂停、回调等全部 typed.js 能力。
- 详细参数与事件请参考 [typed.js 文档](https://github.com/mattboldt/typed.js#customization)。

---

## License

MIT

---

> 本库 fork 自 [mattboldt/typed.js](https://github.com/mattboldt/typed.js)，并在其基础上做了速度和批量输出增强。
