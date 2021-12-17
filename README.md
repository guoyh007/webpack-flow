# webpack-flow

> webpack打包事件流(理论概述)
```
1. 初始化参数：从配置文件和 Shell 语句中读取并合并参数,得出最终的配置对象
1. 用上一步得到的参数初始化 Compiler 对象
1. 加载所有配置的插件
1. 执行 Compiler 对象的 run 方法开始执行编译
1. 根据配置中的entry找出入口文件
1. 从入口文件出发,调用所有配置的Loader对模块进行编译，然后还经过 bable 的解析、转换、生成，才的到最后编译后的代码
1. 再找出该模块依赖的模块，再递归本步骤直到所有入口依赖的文件都经过了本步骤的处理
1. 根据入口和模块之间的依赖关系，组装成一个个包含多个模块的 Chunk
1. 再把每个 Chunk 转换成一个单独的文件加入到输出列表
1. 在确定好输出内容后，根据配置确定输出的路径和文件名，把文件内容写入到文件系统
```

# 操作步骤
先安装（实践操作）

> npm i webpack webpack-cli babel-types @babel/parser @babel/traverse @babel/generator -D
接着在debugger中运行和调试
