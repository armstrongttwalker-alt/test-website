---
title: FlagOpen 大模型技术开源体系
site:
  hide_outline: true
  hide_toc: true
  hide_title_block: true
---

```{dropdown} 点击查看页面CSS样式
:icon: css
:animate: fade-in-slide-down

```{code-block} css
:linenos:

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
  margin-bottom: 1rem;
  flex-grow: 1;
}

/* 卡片链接样式 */
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

/* sphinx-design卡片样式覆盖 */
.sd-card {
  background: var(--card-bg) !important;
  border: 1px solid var(--card-border) !important;
  border-radius: 12px !important;
  padding: 2rem !important;
  height: 100%;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important;
  position: relative;
  overflow: hidden;
}

.sd-card:hover {
  transform: translateY(-4px) !important;
  box-shadow: 0 20px 40px rgba(30, 107, 255, 0.1) !important;
  border-color: var(--flagos-blue) !important;
}

.sd-card::before {
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

.sd-card:hover::before {
  opacity: 1;
}

/* 网格布局调整 */
.sd-gutter-3 {
  gap: 2rem !important;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .flagos-header h1 {
    font-size: 2.25rem;
  }
  
  .flagos-header p {
    font-size: 1.125rem;
  }
  
  .sd-grid {
    grid-template-columns: 1fr !important;
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

/* CTA区域样式 */
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

.flagos-cta .sd-btn {
  display: inline-flex !important;
  align-items: center !important;
  gap: 0.75rem !important;
  background: var(--flagos-blue) !important;
  color: white !important;
  padding: 0.875rem 1.75rem !important;
  border-radius: 8px !important;
  text-decoration: none !important;
  font-weight: 500 !important;
  transition: all 0.2s ease !important;
  border: 2px solid transparent !important;
}

.flagos-cta .sd-btn:hover {
  background: var(--flagos-blue-dark) !important;
  transform: translateY(-2px) !important;
  box-shadow: 0 8px 16px rgba(30, 107, 255, 0.2) !important;
}