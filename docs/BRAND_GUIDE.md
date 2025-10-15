# MPC Brand Guide

**Simple guide for consistent design** - Only the essentials for beginners.

---

## 🎨 Brand Colors

### Main Colors

```
MPC Green:  #00A859  (Primary brand color)
MPC Gold:   #FFD700  (Accent color)
```

### How to Use in Tailwind

```html
<!-- Green (primary) -->
<div class="bg-primary-500 text-white">Content</div>

<!-- Gold (accent) -->
<div class="bg-golden-500 text-gray-900">Content</div>
```

**That's it!** Use `primary-500` for green and `golden-500` for gold.

---

## 🌐 Bilingual Content (Required)

**Always include both English and French:**

```html
<h2 class="text-3xl font-bold">
  <span class="lang-content lang-en active">Welcome</span>
  <span class="lang-content lang-fr">Bienvenue</span>
</h2>
```

**Rules:**

- English has `active` class
- French does NOT have `active` class
- Both must exist for all user-facing text

---

## 🎯 Common Components

### Button

```html
<button class="bg-primary-500 text-white px-6 py-2 rounded-lg hover:bg-primary-600">
  Click Me
</button>
```

### Card

```html
<div class="bg-white rounded-lg shadow-lg p-6">Card content here</div>
```

---

## ✅ Quick Checklist

Before submitting:

- [ ] Using `bg-primary-500` (green) or `bg-golden-500` (gold)
- [ ] All text is bilingual (EN/FR)
- [ ] Tested on mobile (375px width)

---

**That's all you need!** Keep it simple and consistent. 🇲🇷💻
