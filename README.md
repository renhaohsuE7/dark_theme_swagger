# dark_theme_swagger
Da-da-da-da-daaaarkkkkkkkkkkuuuuuu

## example

1. 新增書籤
2. 名稱隨便
3. 網址填：

```
javascript:alert('Hello');
```

點擊書籤 → 會在目前頁面跳出 alert。

## setup


```js
javascript:(function () {
  const id = 'swagger-dark-mode';
  const old = document.getElementById(id);
  if (old) {
    old.remove();
    return;
  }

  const style = document.createElement('style');
  style.id = id;
  style.innerHTML = `
    /* ===== 基礎背景 ===== */
    html, body {
      background: #0b0f14 !important;
      color: #f0f6fc !important;
    }

    .swagger-ui,
    .swagger-ui .wrapper {
      background: #0b0f14 !important;
      color: #f0f6fc !important;
    }

    /* ===== 區塊背景 ===== */
    .swagger-ui .opblock,
    .swagger-ui .scheme-container {
      background: #161b22 !important;
      color: #f0f6fc !important;
    }

    .swagger-ui .opblock-summary,
    .swagger-ui .opblock-body,
    .swagger-ui .opblock-description-wrapper {
      background: #161b22 !important;
      color: #f0f6fc !important;
    }

    /* ===== 文字亮度強化 ===== */
    .swagger-ui,
    .swagger-ui p,
    .swagger-ui span,
    .swagger-ui label,
    .swagger-ui td,
    .swagger-ui th,
    .swagger-ui h1,
    .swagger-ui h2,
    .swagger-ui h3,
    .swagger-ui h4,
    .swagger-ui h5 {
      color: #f0f6fc !important;
    }

    /* 次要說明文字 */
    .swagger-ui .parameter__name,
    .swagger-ui .parameter__type,
    .swagger-ui .response-col_status {
      color: #c9d1d9 !important;
    }

    /* ===== Input / Try it out ===== */
    .swagger-ui input,
    .swagger-ui textarea,
    .swagger-ui select {
      background: #0b0f14 !important;
      color: #f0f6fc !important;
      border-color: #30363d !important;
    }

    /* ===== Code block ===== */
    .swagger-ui pre,
    .swagger-ui code,
    .swagger-ui .highlight-code {
      background: #0d1117 !important;
      color: #e6edf3 !important;
    }

    /* ===== 表格 ===== */
    .swagger-ui table thead tr th {
      color: #f0f6fc !important;
      border-bottom: 1px solid #30363d !important;
    }

    .swagger-ui table tbody tr td {
      color: #e6edf3 !important;
      border-top: 1px solid #21262d !important;
    }
    
    .swagger-ui .opblock-summary-description {
        color: #c6cfd8 !important;
    }

    .swagger-ui .opblock-title span {
      color: #f0f6fc !important;
      font-weight: 600;
    }

    .swagger-ui .btn.try-out__btn {
      background: #21262d !important;
      color: #f0f6fc !important;
      border: 1px solid #30363d !important;
    }

    .swagger-ui .btn.try-out__btn:hover {
      background: #30363d !important;
    }

    .swagger-ui .opblock-section-header {
      background: #161b22 !important;
      border-bottom: 1px solid #30363d !important;
    }

    .swagger-ui .renderedMarkdown,
    .swagger-ui .renderedMarkdown p,
    .swagger-ui .renderedMarkdown li {
      color: #f0f6fc !important;
    }

    .swagger-ui .tab li button {
      color: #c9d1d9 !important;
    }

    .swagger-ui .tab li.active button {
      color: #ffffff !important;
      border-bottom: 2px solid #58a6ff;
    }

  `;

  document.head.appendChild(style);
})();
```