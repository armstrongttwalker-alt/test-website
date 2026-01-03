---
title: FlagOpen 大模型技术开源体系
site:
  hide_outline: true
  hide_toc: true
  hide_title_block: true
---

<style>
/* 导入字体 */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');

:root {
  --flagos-blue: #1e6bff;
  --flagos-blue-dark: #0a4dbf;
  --flagos-blue-light: #e8f1ff;
  --flagos-gray-100: #f8f9fa;
  --flagos-gray-200: #e9ecef;
  --flagos-gray-800: #343a40;
  --flagos-text: #212529;
  --flagos-text-light: #6c757d;
  
  /* 添加卡片背景变量 */
  --card-bg: white;
  --card-border: var(--flagos-gray-200);
}

* {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
}

/* 页面头部样式 */
.flagos-header {
  text-align: center;
  margin: 0 auto 4rem;
  max-width: 800px;
  padding: 0 1rem;
}

.flagos-header h1 {
  font-size: 3rem;
  font-weight: 700;
  color: var(--flagos-text);
  margin-bottom: 1rem;
  line-height: 1.2;
}

.flagos-header p {
  font-size: 1.25rem;
  color: var(--flagos-text-light);
  line-height: 1.6;
  font-weight: 400;
}

/* 网格布局 - 完全复制flagos.io的3列布局 */
.flagos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 2rem;
  margin: 0 auto;
  max-width: 1200px;
}

/* 卡片样式 - 完全匹配flagos.io */
.flagos-card {
  background: var(--card-bg);
  border-radius: 12px;
  border: 1px solid var(--card-border);
  padding: 2rem;
  height: 100%;
  display: flex;
  flex-direction: column;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.flagos-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 40px rgba(30, 107, 255, 0.1);
  border-color: var(--flagos-blue);
}

.flagos-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, var(--flagos-blue), #4dabff);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.flagos-card:hover::before {
  opacity: 1;
}

/* 图标样式 */
.card-icon-wrapper {
  width: 56px;
  height: 56px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  background: var(--flagos-blue-light);
}

.card-icon {
  font-size: 1.5rem;
  font-weight: 700;
  background: linear-gradient(135deg, var(--flagos-blue), var(--flagos-blue-dark));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* 卡片标题 */
.card-title {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--flagos-text);
  margin-bottom: 1rem;
  line-height: 1.3;
}

/* 卡片描述 */
.card-description {
  color: var(--flagos-text-light);
  line-height: 1.6;
  margin-bottom: 2rem;
  flex-grow: 1;
}

/* 卡片底部链接按钮 - 匹配flagos.io按钮样式 */
.card-footer {
  margin-top: auto;
}

.card-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--flagos-blue);
  text-decoration: none;
  font-weight: 500;
  padding: 0.5rem 0;
  border-bottom: 2px solid transparent;
  transition: all 0.2s ease;
}

.card-link:hover {
  color: var(--flagos-blue-dark);
  border-bottom-color: var(--flagos-blue);
}

.card-link::after {
  content: '→';
  font-size: 1.25em;
  transition: transform 0.2s ease;
}

.card-link:hover::after {
  transform: translateX(4px);
}

/* 响应式设计 */
@media (max-width: 768px) {
  .flagos-header h1 {
    font-size: 2.25rem;
  }
  
  .flagos-header p {
    font-size: 1.125rem;
  }
  
  .flagos-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}

/* 主题切换支持 */
@media (prefers-color-scheme: dark) {
  :root {
    --flagos-blue: #4dabff;
    --flagos-blue-dark: #1e6bff;
    --flagos-blue-light: rgba(30, 107, 255, 0.1);
    --flagos-gray-100: #1a1d1e;
    --flagos-gray-200: #2d3236;
    --flagos-gray-800: #f8f9fa;
    --flagos-text: #f8f9fa;
    --flagos-text-light: #adb5bd;
    --card-bg: var(--flagos-gray-100);
    --card-border: var(--flagos-gray-200);
  }
}

/* 使用Sphinx主题变量覆盖 */
.sd-card {
  border: none !important;
  box-shadow: none !important;
  background: transparent !important;
}

/* 添加底部CTA容器的样式 */
.flagos-cta {
  text-align: center;
  margin: 4rem auto 0;
  padding: 3rem 2rem;
  background: linear-gradient(135deg, var(--flagos-blue-light), rgba(30, 107, 255, 0.05));
  border-radius: 16px;
  max-width: 800px;
}

.flagos-cta h2 {
  font-size: 2rem;
  font-weight: 600;
  color: var(--flagos-text);
  margin-bottom: 1rem;
}

.flagos-cta p {
  color: var(--flagos-text-light);
  margin-bottom: 2rem;
  line-height: 1.6;
  font-size: 1.125rem;
}

.flagos-cta a {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  background: var(--flagos-blue);
  color: white;
  padding: 0.875rem 1.75rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.2s ease;
  border: 2px solid transparent;
}

.flagos-cta a:hover {
  background: var(--flagos-blue-dark);
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(30, 107, 255, 0.2);
}
</style>

<div class="flagos-header">
  <h1>FlagOpen 大模型技术开源体系</h1>
  <p>一套完整的 AI 开发工具链，为人工智能模型开发与部署提供全方位支持，助力国产 AI 芯片生态建设</p>
</div>

<div class="flagos-grid">
  <!-- FlagGems -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">FG</span>
    </div>
    <h3 class="card-title">FlagGems</h3>
    <div class="card-description">
      基于 Triton 的高性能通用算子库，为大模型提供跨平台的高性能算子实现，加速模型推理与训练过程。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>

  <!-- FlagTree -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">FT</span>
    </div>
    <h3 class="card-title">FlagTree</h3>
    <div class="card-description">
      面向多元 AI 芯片的编译器平台，提供统一的 Triton 生态支持，简化模型在不同硬件上的部署复杂度。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>

  <!-- FlagScale -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">FS</span>
    </div>
    <h3 class="card-title">FlagScale</h3>
    <div class="card-description">
      全流程大模型工具集，支持从训练到部署的完整生命周期管理，提供企业级的大模型解决方案。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>

  <!-- FlagCX -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">CX</span>
    </div>
    <h3 class="card-title">FlagCX</h3>
    <div class="card-description">
      自适应跨芯片通信库，提供高性能的点对点与集合通信能力，优化分布式训练和推理性能。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>

  <!-- KernelGen -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">KG</span>
    </div>
    <h3 class="card-title">KernelGen</h3>
    <div class="card-description">
      算子自动生成工具，通过自然语言描述自动生成优化算子，大幅提升开发效率与代码质量。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>

  <!-- FlagRelease -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">FR</span>
    </div>
    <h3 class="card-title">FlagRelease</h3>
    <div class="card-description">
      自动化模型迁移与发布平台，提供标准化的多芯片适配流程，降低模型迁移成本与风险。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>

  <!-- FlagPerf -->
  <div class="flagos-card">
    <div class="card-icon-wrapper">
      <span class="card-icon">FP</span>
    </div>
    <h3 class="card-title">FlagPerf</h3>
    <div class="card-description">
      AI 硬件评测引擎，建立产业实践导向的指标体系，全面评估芯片在实际场景中的性能表现。
    </div>
    <div class="card-footer">
      <a href="#" class="card-link">了解更多</a>
    </div>
  </div>
</div>

<div class="flagos-cta">
  <h2>开始使用 FlagOpen</h2>
  <p>加入我们，共同构建开放的 AI 芯片开发生态系统</p>
  <a href="#">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M12 6V18M18 12L6 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    查看完整文档
  </a>
</div>
