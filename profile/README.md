<div align="center"> 
  
# `✨ Jvavscratch`

**实时将JavaScript代码转换为可用的Scratch项目。** 

<img width="256" height="256" alt="image" src="https://bgithub.xyz/user-attachments/assets/cc117258-a2a6-451a-99d3-47c1ae1a254a" />
</div>

---

## 关于Jvavscratch

Jvavscratch是一个创新的开源项目，旨在桥接JavaScript和Scratch之间的鸿沟，让编程学习和创作更加简单高效。通过Jvavscratch，您可以使用熟悉的JavaScript语法编写代码，然后实时转换为Scratch项目，充分发挥两种平台的优势。

### 核心特性

- **实时转换**：编写JavaScript代码，立即生成对应的Scratch积木
- **完整的JavaScript支持**：支持大部分JavaScript语法特性，包括函数、类、事件等
- **模块化开发**：支持项目模块化，便于大型项目管理
- **扩展性强**：提供丰富的API和工具，支持自定义功能扩展
- **开发友好**：支持热重载、错误提示等开发体验优化功能

## 快速开始

### 前置条件

**本项目要求您安装以下工具：**
- [Node.js](https://nodejs.org)（版本 >= 16）

### 安装与使用

1. **克隆仓库**
   ```bash
   git clone https://github.com/Jvavscratch/jvavscratch.git
   cd jvavscratch
   ```

2. **安装依赖**
   ```bash
   npm install
   ```

3. **创建新项目**
   ```bash
   node src/index.js new my-first-project
   ```

4. **运行项目**
   ```bash
   cd my-first-project
   node ../src/index.js run
   ```

### 基本命令

- `node src/index.js init`: 在当前目录创建项目
- `node src/index.js new [name] [path]`: 创建新的指定名称的项目
- `node src/index.js run`: 构建并运行当前项目
- `node src/index.js build`: 仅构建当前项目
- `node src/index.js add [...lib]`: 添加库/依赖
- `node src/index.js update`: 更新项目依赖

## 项目结构

一个典型的Jvavscratch项目结构如下：

```
my-project:
    > assets          # 角色和舞台资源
        > Sprite1...  # 角色资源
        > stage...    # 舞台资源
    > lib             # 第三方库
    > src             # JavaScript源代码
        > Sprite1.js  # 角色代码
    > target          # 构建输出目录
    > project.d.json  # 项目配置文件
```

## 文档

完整的文档可在[Jvavscratch文档网站](https://jvavscratch.github.io/docs/)找到，包括：

- **入门指南**：从零开始学习Jvavscratch
- **语法教程**：JavaScript到Scratch的映射规则
- **API参考**：所有可用API的详细文档
- **模块说明**：核心模块的使用方法

## 社区

加入Jvavscratch社区，与其他开发者一起交流学习：

- **GitHub讨论区**：在[Issues](https://github.com/Jvavscratch/discussion)中提问和讨论

## 许可证

Jvavscratch基于[MPL-2.0](LICENSE)开源协议。

## 贡献者

感谢所有为Jvavscratch做出贡献的开发者！

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：

- **GitHub**：[https://github.com/Jvavscratch](https://github.com/Jvavscratch)
- **邮箱**：2913335827@qq.com

---

<div align="center">
  <p>Made with ❤️ by the Jvavscratch Team</p>
  <p>让编程学习更简单！</p>
</div>
