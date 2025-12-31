---
title: Welcome to My Landing Page
site:
  hide_outline: true
  hide_toc: true
  hide_title_block: true
---

<style>
/* 自定义样式 */
:root {
  --primary-color: #2563eb;
  --secondary-color: #7c3aed;
  --accent-color: #059669;
  --card-bg: #ffffff;
  --card-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --card-shadow-hover: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* 页面标题样式 */
.landing-header {
  text-align: center;
  margin-bottom: 3rem;
  padding: 2rem 1rem;
  background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
  border-radius: 1rem;
  border-left: 4px solid var(--primary-color);
}

.landing-header h1 {
  color: #1e293b;
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.landing-header p {
  color: #64748b;
  font-size: 1.125rem;
  max-width: 600px;
  margin: 0 auto;
}

/* 卡片增强样式 */
.sd-card {
  transition: all 0.3s ease;
  border: 1px solid #e2e8f0;
  border-radius: 12px;
  overflow: hidden;
  height: 100%;
  background: var(--card-bg) !important;
  box-shadow: var(--card-shadow) !important;
  position: relative;
}

.sd-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--card-shadow-hover) !important;
  border-color: var(--primary-color);
}

.sd-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  opacity: 0;
  transition: opacity 0.3s ease;
}

.sd-card:hover::before {
  opacity: 1;
}

.sd-card-header {
  padding: 1.5rem 1.5rem 0.5rem;
  border-bottom: none !important;
}

.sd-card-title {
  font-size: 1.25rem !important;
  font-weight: 600 !important;
  color: #1e293b !important;
  margin-bottom: 0.75rem !important;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

/* 卡片图标 */
.card-icon {
  width: 32px;
  height: 32px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: white;
  font-size: 0.875rem;
  flex-shrink: 0;
}

.icon-gem { background: linear-gradient(135deg, #8b5cf6, #7c3aed); }
.icon-tree { background: linear-gradient(135deg, #10b981, #059669); }
.icon-scale { background: linear-gradient(135deg, #3b82f6, #2563eb); }
.icon-connect { background: linear-gradient(135deg, #f59e0b, #d97706); }
.icon-magic { background: linear-gradient(135deg, #ec4899, #db2777); }
.icon-rocket { background: linear-gradient(135deg, #06b6d4, #0891b2); }
.icon-chart { background: linear-gradient(135deg, #f97316, #ea580c); }

.sd-card-body {
  padding: 0.5rem 1.5rem 1rem;
  color: #64748b;
  line-height: 1.6;
}

.sd-card-footer {
  padding: 1rem 1.5rem 1.5rem;
  background: transparent !important;
  border-top: 1px solid #f1f5f9 !important;
}

.sd-card-footer a {
  display: inline-flex;
  align-items: center;
  gap: 0.375rem;
  padding: 0.5rem 1rem;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  color: white !important;
  text-decoration: none;
  border-radius: 6px;
  font-weight: 500;
  transition: all 0.2s ease;
  border: none;
}

.sd-card-footer a:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
}

/* 响应式调整 */
@media (max-width: 768px) {
  .landing-header h1 {
    font-size: 2rem;
  }
  
  .landing-header p {
    font-size: 1rem;
  }
  
  .sd-card {
    margin-bottom: 1rem;
  }
}
</style>

<div class="landing-header">
  <h1>FlagOpen 生态工具集</h1>
  <p>一套完整的AI开发工具链，为人工智能模型开发与部署提供全方位支持</p>
</div>

::::{grid} 1 2 3 3
:gutter: 3

:::{grid-item-card} 
:link: 
:link-type: url

**FlagGems** <span class="card-icon icon-gem">FG</span>
^^^
FlagGems 是一款使用Triton编程语言及其扩展语言实现的高性能通用算子库。旨在为大模型提供一系列通用算子，加速模型面向多种后端平台的推理与训练。
+++
[了解更多 →](#)
:::

:::{grid-item-card} 
:link: 
:link-type: url

**FlagTree** <span class="card-icon icon-tree">FT</span>
^^^
FlagTree 是一款面向多种 AI 芯片的开源、统一编译器。致力于打造多元 AI 芯片编译器及相关工具平台，发展和壮大Triton 上下游生态。
+++
[了解更多 →](#)
:::

:::{grid-item-card} 
:link: 
:link-type: url

**FlagScale** <span class="card-icon icon-scale">FS</span>
^^^
FlagScale 是一款全流程大模型工具集，可支持大模型的完整生命周期管理。依托主流开源项目的技术优势，为大模型的管理与规模化部署提供端到端解决方案。
+++
[了解更多 →](#)
:::

:::{grid-item-card} 
:link: 
:link-type: url

**FlagCX** <span class="card-icon icon-connect">CX</span>
^^^
FlagCX 是一款可扩展、自适应的跨芯片统一通信库。面向多芯片、多平台场景，提供高性能的点对点与集合通信能力。
+++
[了解更多 →](#)
:::

:::{grid-item-card} 
:link: 
:link-type: url

**KernelGen** <span class="card-icon icon-magic">KG</span>
^^^
KernelGen 是一款算子自动生成工具。通过自然语言提示构建算子定义，自动完成算子准确率及性能测试，生成Triton算子。
+++
[了解更多 →](#)
:::

:::{grid-item-card} 
:link: 
:link-type: url

**FlagRelease** <span class="card-icon icon-rocket">FR</span>
^^^
FlagRelease 是一款面向多架构人工智能芯片的大模型的自动迁移、适配与发布平台。通过自动化、标准化和智能化的适配流程，使主流大模型能够在不同国产人工智能芯片上高效完成模型迁移。
+++
[了解更多 →](#)
:::

:::{grid-item-card} 
:link: 
:link-type: url

**FlagPerf** <span class="card-icon icon-chart">FP</span>
^^^
FlagPerf是一款一体化AI硬件评测引擎。旨在建立以产业实践为导向的指标体系，评测AI硬件在软件栈组合下的实际能力。
+++
[了解更多 →](#)
:::

:::{grid-item-card} FlagTree
:link: 
:link-type: url
:class: has-icon-tree

<span class="card-icon">FT</span>
^^^
FlagTree 是一款面向多种 AI 芯片的开源、统一编译器...
+++
[了解更多 →](#)
:::


::::

<div style="text-align: center; margin-top: 3rem; padding: 2rem; background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%); border-radius: 12px;">
  <h3 style="color: #1e293b; margin-bottom: 1rem;">开始使用 FlagOpen 生态</h3>
  <p style="color: #64748b; max-width: 600px; margin: 0 auto 1.5rem;">选择适合您需求的工具，或查看完整文档以了解更多信息</p>
  <a href="#" style="display: inline-flex; align-items: center; gap: 0.5rem; padding: 0.75rem 1.5rem; background: linear-gradient(to right, #059669, #10b981); color: white; text-decoration: none; border-radius: 8px; font-weight: 600; transition: all 0.2s ease;">
    <svg style="width: 20px; height: 20px;" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path>
    </svg>
    查看完整文档
  </a>
</div>