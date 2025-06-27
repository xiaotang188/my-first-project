# ai-develop-assistant
协助AI开发者进行智能化需求完善、模块设计、技术架构设计的MCP工具
# ✨ 优化功能总览
## 🚀 MCP AI开发助手 - 智能需求分析与架构设计
## ✨ 核心特性
### 🧠 智能分支感知系统
1. 分支识别: 自动识别当前讨论的需求分支（项目目标、功能设计、技术偏好、UI设计）
2. 记忆保持: 防止AI在多轮对话中遗忘未完成的需求维度
3. 渐进式澄清: 确保所有核心需求分支都得到充分讨论
4. 智能提醒: 自动提醒未完成的需求分支，防止遗漏

### 🤖 AI自主设计与控制
1. 用户授权检测: 识别"常规设计"、"标准方案"等用户授权AI自主设计的表达
2. 分支式设计: 仅对当前分支进行自主设计，不会跳跃到其他未讨论的分支
3. 完整性门控: 只有所有核心分支完成后才允许进入架构设计阶段
4. AI自我评估: AI主动评估自己对需求的理解深度，不足时拒绝架构设计

# 🚀 MCP AI开发助手 - 最终配置指南
### 🔧 核心工具 (5个)
1. **requirement_clarifier** - 需求澄清助手
2. **requirement_manager** - 需求文档管理器
3. **architecture_designer** - 架构设计生成器
4. **export_final_document** - 导出完整文档 ⭐ 新增
5. **view_requirements_status** - 查看需求状态 ⭐ 新增

### 💾 持久化存储特性
- ✅ **自动保存**: 每次操作都会自动保存到文件
- ✅ **历史记录**: 完整的操作历史追溯
- ✅ **多格式导出**: JSON + Markdown双格式
- ✅ **自定义目录**: 支持环境变量配置存储位置

## 📁 配置方法

### 方法1: Claude Desktop配置 (推荐)

1. **找到配置文件位置**
   ```
   Windows: %APPDATA%\Claude\claude_desktop_config.json
   macOS: ~/Library/Application Support/Claude/claude_desktop_config.json
   Linux: ~/.config/claude/claude_desktop_config.json
   ```

2. **添加配置内容**
   ```json
   {
     "mcpServers": {
       "ai-develop-assistant": {
         "command": "python",
         "args": [
           "path\AIDevlopStudy.py"
         ],
         "env": {
           "MCP_STORAGE_DIR": "your save path"
         }
       }
     }
   }
   ```

3. **重启Claude Desktop**

### 方法2: 环境变量配置

创建 `.env` 文件：
```bash
# 自定义存储目录
MCP_STORAGE_DIR=./mcp_data

# 或者设置为其他路径
# MCP_STORAGE_DIR=D:/MyProjects/mcp_storage
```

## 📊 存储结构

配置成功后，会在指定目录生成以下文件：

```
mcp_data/
├── requirements.json      # 实时需求文档
├── history.json          # 操作历史记录
├── final_document_*.json # 导出的完整文档
└── final_document_*.md   # Markdown格式报告
```

## 🎯 使用流程

### 完整的项目分析流程

1. **需求澄清阶段**
   ```
   requirement_clarifier("我要做一个WebAI资源分享网站")
   ↓
   requirement_manager("项目类型：Web应用...", "项目概述")
   ↓
   view_requirements_status() # 查看当前状态
   ```

2. **架构设计阶段**
   ```
   architecture_designer("WebAI资源分享网站架构")
   ↓
   view_requirements_status() # 确认完整性
   ```

3. **文档导出阶段**
   ```
   export_final_document() # 导出完整项目文档
   ```

## 🧪 测试验证

运行测试脚本验证配置：
```bash
# 激活虚拟环境
.venv\Scripts\activate

# 运行测试
python test_optimized_mcp.py
```

预期输出：
```
🧪 测试优化后的MCP AI开发助手...
📁 存储目录: test_mcp_data
✅ 发现 5 个工具
✅ 所有功能测试成功
✅ 生成了 4 个文件
🎉 优化版MCP测试完成!
```

## 💡 使用技巧

### 1. 项目开始前
- 设置好 `MCP_STORAGE_DIR` 环境变量
- 确保目录有写入权限

### 2. 需求分析中
- 定期使用 `view_requirements_status` 查看进度
- 每次澄清后都会自动保存

### 3. 项目完成后
- 使用 `export_final_document` 导出完整文档
- Markdown文件可作为项目README基础

### 4. 多项目管理
- 为不同项目设置不同的存储目录
- 使用项目名称作为目录名

## 🔍 故障排除

### 常见问题

1. **存储目录权限问题**
   ```bash
   # 确保目录可写
   mkdir -p ./mcp_data
   chmod 755 ./mcp_data
   ```

2. **环境变量未生效**
   ```bash
   # 检查环境变量
   echo $MCP_STORAGE_DIR
   
   # 重新设置
   export MCP_STORAGE_DIR="./mcp_data"
   ```

3. **文件编码问题**
   - 所有文件使用UTF-8编码
   - 支持中文内容

## 🎉 优势总结

### 相比原版的改进
- ✅ **数据持久化**: 不再丢失分析结果
- ✅ **历史追溯**: 完整的操作记录
- ✅ **文档导出**: 自动生成项目文档
- ✅ **状态查看**: 实时了解分析进度
- ✅ **配置灵活**: 自定义存储位置

### 实际价值
- 🚀 **提升效率**: 避免重复分析
- 📋 **文档完整**: 自动生成项目文档
- 🔄 **过程可控**: 随时查看分析状态
- 💾 **数据安全**: 本地存储，隐私保护

---

**🎯 现在您的MCP AI开发助手已经完全优化，支持持久化存储和完整的项目文档管理！**

开始使用：
1. 配置Claude Desktop
2. 重启Claude Desktop  
3. 开始您的AI项目分析之旅！

