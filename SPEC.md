# 作业小管家 - SPEC.md

## Concept & Vision
一个简洁的家庭作业管理网页，给家里两个小朋友（悠悠和Sunday）分别追踪每日作业和重要安排。界面干净清爽，像一张干净的学习清单，家长和孩子都能一眼看清今天要做什么。

## Design Language
- **Aesthetic**: 简洁卡片式设计，每个小朋友一张卡片，当天的作业一目了然
- **Color Palette**:
  - Primary: #4A90D9 (蓝色 - 悠悠)
  - Secondary: #E8A87C (橙色 - Sunday)
  - Background: #F7F9FC
  - Card: #FFFFFF
  - Text: #2C3E50
  - Done: #52C41A
  - Due: #FF6B6B
- **Typography**: "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", sans-serif
- **Motion**: 作业完成时打勾动画，添加作业时卡片滑入

## Layout & Structure
- **Header**: 当前日期 + 页面标题
- **Body**: 两列卡片（手机端单列堆叠）
  - 悠悠的卡片（蓝色主题）
  - Sunday的卡片（橙色主题）
- **每张卡片包含**:
  - 姓名 + 头像emoji
  - 今日作业列表
  - 重要安排
  - 添加作业按钮
- **Footer**: 最后更新时间

## Features & Interactions
1. **作业列表**: 显示今日作业，可勾选完成
2. **完成打卡**: 勾选后划线+变灰，有动画
3. **添加作业**: 点击按钮弹出输入框
4. **重要安排**: 单独区块显示当天重要事项
5. **本地存储**: 数据保存在浏览器本地，不用登录
6. **每日自动清空**: 新的一天作业列表自动清空（保留已完成记录）

## Component Inventory
1. **KidCard**: 小朋友卡片容器
2. **AssignmentList**: 作业列表（可勾选）
3. **EventBadge**: 重要安排标签
4. **AddButton**: 添加按钮
5. **AddModal**: 添加作业/安排的弹窗

## Technical Approach
- 纯前端单HTML文件
- LocalStorage 存储数据
- 响应式设计（手机/电脑都能用）
- 部署在 Netlify（用户已有账户）
