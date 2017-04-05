# How to Test React Components Using Jest

A repository written for a [blog post about testing React with Jest](https://www.sitepoint.com/test-react-components-jest).

## Requirements

* [Node.js](http://nodejs.org/)

## Running locally

- `git clone` this repo
- `cd testing-react-with-jest`
- `npm install`
- In one tab, run `npm run watch`. This will fire up Webpack and rebuild your app on each change.
- In another tab, run `npm start`. This will fire up a local server that will refresh automatically when the code changes.
- `open http://localhost:8081` to view to the app.

## Tests

Run `npm test` to run the tests with Jest.

Run `npm test -- --watch` to run Jest and have it automatically rerun everytime you change a file.

## Problems / Questions

Please feel free to raise an issue if you have any Qs :)


## License

The MIT License (MIT)

Copyright (c) 2016 SitePoint

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

***

#### [jest](http://facebook.github.io/jest/docs/using-matchers.html#content)
- 功能性测试
- 非功能性的问题：
	1. 兼容性、
	1. 性能、
	1. 安全性
- [探索性测试](http://blog.csdn.net/ant_ren/article/details/8230290)

***

#### 特点：
- 默认使用Jasmine断言
- 模块化的
- 可扩展的
- 可配置的
- 默认自动模拟所有模块，便于测试当前代码
- 虚拟化JS环境，模拟浏览器
- 并行运行工作线程

- 集成Babel - babel-jest babel-polyfill
- `__mocks__`目录,手动模拟文件
- 生成覆盖率报表 jest –coverage

- test 命令是 package 的一项默认字段：
	npm test
	```
	"scripts": {
	    "test": "jest"
	},
	```

	npm run test-jest
	```
	"scripts": {
	    "test-jest": "jest"
	},
	```

- Using with npm scripts #

```
jest -u -t="ColorPicker"
等同于
npm test -- -u -t="ColorPicker"
```


#### 关键字
- describe
- expect
- toBe 对于原始类型，如字符串和数字
- toEqual 是用于处理`数组`和对象的，它会递归的比较给定对象的所有字段或者元素以确认相等
- jest中的 test 方法只是 it 的一个别名
- jest.fn() 监听方法，是无需关注其实现，只需考虑其调用时机及方式的方法
- toMatchSnapshot

- [如何使用 Jest 测试 React 组件](https://www.oschina.net/translate/test-react-components-jest?utm_source=tuicool&utm_medium=referral)
	- 如果你在使用其它框架对  Babel, React 和 JSX 进行测试时遇到过挫折，那么我绝对会推荐你尝试一下 Jest
	* 如果你发现现有的测试设置太慢了，我也会强烈推荐Jest
	* 内置的MOCK测试，SPY测试以及STUB测试
	* npm test -- --watch
	* 测试React组件
		* 测试渲染正确的数据
		* 测试React的交互
		* 快照输出
