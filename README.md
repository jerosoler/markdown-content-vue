# Markdown content vue

Based on  [@nuxt/content](https://github.com/nuxt/content) code.

View instructions on [link](https://content.nuxtjs.org/writing#markdown)

# Features
- Parse content
- Html
- Vue components
- Codeblocks (Prismjs)

# Install
```
npm install markdown-content-vue --save
```

# Usage

### Import
```javascript
import { markdownContent, markdownParse } from 'markdown-content-vue'
```

### Template
```html
<markdownContent :document="code" />
```

### Script
Register component
```javascript
components: {
    markdownContent
}
```
And parse Markdown
```javascript
async mounted() {
    const md = new markdownParse()
    const file = '---\ntitle: test\n---\n# Hello World\n ```javascript\n console.log("Hello") \n```\n<HelloWorld></HelloWorld> \n'
    this.code = await md.toJSON(file)
    console.log(this.code)
  },
  ```


# Beautiful example

### Install github-markdown-css
```
npm install github-markdown-css
```

### Import
```javascript
import 'github-markdown-css/github-markdown.css'
import 'prismjs/themes/prism-tomorrow.css'
```

### Template
```html
<markdownContent class="markdown-body" :document="code" />
```





