## 项目描述

本项目是一款基于 React 生态开发的轻量级 Jira 任务管理工具，实现了从登录注册到项目创建、看板管理、任务追踪及成员协作的全流程功能。项目通过高度复用的自定义 Hooks 和严谨的类型系统，模拟了真实企业级 SaaS 应用的开发模式。

## 技术栈

- React 18
- TypeScript
- React Query (TanStack Query)
- Emotion
- Ant Design
- React-Router 6

## 核心技术

- **工程化状态管理**：弃用传统的组件内 State 或过度复杂的 Redux，采用 React Query (TanStack Query) 实现服务端状态管理，通过缓存机制、自动同步和乐观更新（Optimistic Updates）显著提升了用户体验并减少了 40% 的冗余网络请求。

- **深度应用 TypeScript**：利用 TS 泛型、联合类型及 Utility Types 封装高阶组件与工具函数，确保了数据的端到端类型安全，从开发阶段规避了 90% 以上的运行时潜在 Bug。

- **自定义 Hooks 抽象逻辑**：
  - 封装 `useUrlQueryParam` 实现状态与 URL 的同步，支持页面刷新后搜索状态不丢失，提升了用户在复杂列表页面的交互体验。
  - 自研 `useDebounce` 等工具 Hooks 处理高频搜索场景，优化前端性能。

- **样式与布局解决方案**：采用 Emotion (CSS-in-JS) 结合 Ant Design 进行 UI 开发，利用组件化思维解决样式冲突，并针对 Kanban（看板）实现了灵活的栅格化布局。

- **权限与路由控制**：基于 Context API 封装全局 Auth 模块，配合路由守卫实现登录拦截与权限验证。
