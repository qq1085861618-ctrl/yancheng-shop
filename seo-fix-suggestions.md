# 岩城星选 - 技术SEO修复方案

## 一、高优先级修复项

### 1. 修复Title编码问题并添加Meta标签

**在 `<head>` 标签内添加：**

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>岩城星选 - 精选岩城特产 | 天然农产品礼品定制</title>
<meta name="description" content="岩城星选，源自岩城的天然馈赠。精选野生菌菇、农家土蜂蜜、古树普洱茶、滋补养生品等优质农产品，支持礼盒定制，全国配送。">
<meta name="keywords" content="岩城特产,农产品,菌菇干货,土蜂蜜,普洱茶,礼盒定制,天然食品">
<meta name="author" content="岩城星选">
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://www.yanchengxingxuan.com/">
```

---

### 2. 添加Open Graph标签

**在 `<head>` 标签内添加：**

```html
<!-- Open Graph / 微信分享 -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://www.yanchengxingxuan.com/">
<meta property="og:title" content="岩城星选 - 精选岩城特产">
<meta property="og:description" content="源自岩城的天然馈赠，每一份礼物都承载着我们对品质的执着追求。从山野到餐桌，只为您和家人带来最纯粹的美味体验。">
<meta property="og:image" content="https://www.yanchengxingxuan.com/images/og-cover.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:locale" content="zh_CN">
<meta property="og:site_name" content="岩城星选">

<!-- 微信专用 -->
<meta property="weixin:share_title" content="岩城星选 - 精选岩城特产">
<meta property="weixin:share_desc" content="源自岩城的天然馈赠，精选农产品礼盒定制">
<meta property="weixin:share_img" content="https://www.yanchengxingxuan.com/images/wechat-share.jpg">
```

---

### 3. 添加JSON-LD结构化数据

**在 `</head>` 标签前添加：**

```html
<!-- 组织信息 -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "岩城星选",
  "alternateName": "Yancheng Xingxuan",
  "url": "https://www.yanchengxingxuan.com",
  "logo": "https://www.yanchengxingxuan.com/images/logo.png",
  "description": "精选岩城特产，传递心意",
  "address": {
    "@type": "PostalAddress",
    "addressCountry": "CN",
    "addressRegion": "福建省"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+86-400-XXX-XXXX",
    "contactType": "customer service",
    "availableLanguage": ["Chinese"]
  },
  "sameAs": [
    "https://weibo.com/yanchengxingxuan",
    "https://www.xiaohongshu.com/user/yanchengxingxuan"
  ]
}
</script>

<!-- 网站信息 -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "岩城星选",
  "url": "https://www.yanchengxingxuan.com",
  "potentialAction": {
    "@type": "SearchAction",
    "target": "https://www.yanchengxingxuan.com/search?q={search_term_string}",
    "query-input": "required name=search_term_string"
  }
}
</script>

<!-- 产品列表结构化数据示例 -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "name": "岩城星选热销产品",
  "description": "精选岩城特色农产品",
  "numberOfItems": 12,
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@type": "Product",
        "name": "岩城野生红菇",
        "description": "深山野生采摘，汤色红润，口感鲜美",
        "image": "https://www.yanchengxingxuan.com/images/products/honggu.jpg",
        "offers": {
          "@type": "Offer",
          "price": "168",
          "priceCurrency": "CNY",
          "availability": "https://schema.org/InStock"
        }
      }
    },
    {
      "@type": "ListItem",
      "position": 2,
      "item": {
        "@type": "Product",
        "name": "特级竹荪",
        "description": "菌中皇后，脆嫩爽口，营养丰富",
        "image": "https://www.yanchengxingxuan.com/images/products/zhusun.jpg",
        "offers": {
          "@type": "Offer",
          "price": "128",
          "priceCurrency": "CNY",
          "availability": "https://schema.org/InStock"
        }
      }
    }
  ]
}
</script>

<!-- 面包屑导航结构化数据 -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "首页",
      "item": "https://www.yanchengxingxuan.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "全部商品",
      "item": "https://www.yanchengxingxuan.com/products"
    }
  ]
}
</script>
```

---

## 二、中优先级修复项

### 4. 优化语义化HTML结构

**将页面主体内容包裹在 `<main>` 标签中：**

```html
<body>
  <!-- 导航保持不变 -->
  <nav>...</nav>
  
  <!-- 添加main标签 -->
  <main>
    <div id="home" class="page active">
      <!-- 首页内容 -->
    </div>
    <!-- 其他页面 -->
  </main>
  
  <!-- 页脚 -->
  <footer>...</footer>
</body>
```

**使用更语义化的标题层级：**

```html
<!-- 首页 Hero 区域 -->
<section class="hero" aria-label="品牌介绍">
  <h1>岩城星选</h1>
  <p class="subtitle">精选好物，传递心意</p>
</section>

<!-- 产品区域 -->
<section class="products" aria-labelledby="products-title">
  <h2 id="products-title">精选好物</h2>
  <!-- 产品卡片 -->
</section>

<!-- 特色区域 -->
<section class="features" aria-labelledby="features-title">
  <h2 id="features-title">为什么选择岩城星选</h2>
</section>
```

---

### 5. 图片优化建议

**当前问题**：使用emoji代替图片，搜索引擎无法识别。

**建议方案**：

```html
<!-- 将emoji替换为真实图片 -->
<div class="product-card">
  <img 
    src="/images/products/honggu.jpg" 
    alt="岩城野生红菇 - 深山采摘优质菌菇"
    loading="lazy"
    width="160"
    height="160"
  >
  <h3>岩城野生红菇</h3>
  <p class="category">菌菇干货</p>
  <span class="price">¥168</span>
</div>
```

**图片SEO最佳实践**：
- 所有产品图片必须有描述性alt属性
- 使用 `loading="lazy"` 延迟加载
- 添加 `width` 和 `height` 属性防止布局偏移
- 图片文件名使用关键词：`yancheng-wild-mushroom.jpg`

---

## 三、其他SEO优化建议

### 6. 添加网站图标和移动端图标

```html
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="manifest" href="/site.webmanifest">
<meta name="theme-color" content="#8B4513">
```

### 7. 添加Twitter卡片标签

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="岩城星选 - 精选岩城特产">
<meta name="twitter:description" content="源自岩城的天然馈赠，精选农产品礼盒定制">
<meta name="twitter:image" content="https://www.yanchengxingxuan.com/images/twitter-card.jpg">
```

### 8. 添加地理位置标签（本地SEO）

```html
<meta name="geo.region" content="CN-FJ">
<meta name="geo.placename" content="岩城">
<meta name="geo.position" content="26.xxxx;119.xxxx">
<meta name="ICBM" content="26.xxxx, 119.xxxx">
```

---

## 四、修复优先级排序

| 优先级 | 修复项 | 预计工作量 |
|--------|--------|-----------|
| P0 | Title编码修复 | 5分钟 |
| P0 | 添加Meta Description | 10分钟 |
| P0 | 添加Open Graph标签 | 15分钟 |
| P1 | 添加JSON-LD结构化数据 | 30分钟 |
| P1 | 添加canonical标签 | 2分钟 |
| P2 | 语义化HTML优化 | 1小时 |
| P2 | 图片替换为真实图片 | 2-3小时 |
| P3 | 添加网站图标等 | 30分钟 |

---

## 五、预期效果

修复完成后，预期获得以下改善：

1. **搜索结果展示优化**
   - 标题正常显示中文
   - 显示自定义描述文字
   - 可能显示产品评分、价格等富媒体信息

2. **社交分享优化**
   - 微信/微博分享卡片正常显示
   - 控制分享图片和文字展示

3. **搜索引擎理解度提升**
   - 结构化数据帮助搜索引擎理解页面内容
   - 提高产品页面在搜索结果中的可见性

---

生成时间：2026-04-21 15:30
技术SEO检查 - Step2 完成
