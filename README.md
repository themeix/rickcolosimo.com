# RickColosimo.com – Jekyll & Tailwind CSS v4 Static Website

This project is a clean, modern, and high-performance Jekyll website styled with Tailwind CSS v4 and designed for direct content editing via YAML and Markdown files, with automated deployment to GitHub Pages via GitHub Actions.

---

## কিভাবে সাইটের কনটেন্ট এডিট করবেন (How to Edit Content)

কোনো CMS ছাড়াই আপনি খুব সহজে এই সাইটের সবকিছু এডিট করতে পারবেন:

### ১. সাইট সেটিংস, যোগাযোগ ও ফুটার এডিট করা
**ফাইল:** `_data/settings.yml`
- সাইটের নাম, ট্যাগলাইন, বর্ণনা।
- যোগাযোগের ইমেইল (`email`), ফোন নম্বর (`phone`), ঠিকানা (`address`)।
- টুইটার লিঙ্ক ও লেবেল।
- ফুটার ক্রেডিট ও কপিরাইট টেক্সট।

### ২. মেনু ও নেভিগেশন পরিবর্তন করা
**ফাইল:** `_data/navigation.yml`
- হেডারের প্রধান মেনু আইটেম ও ড্রপডাউন সাবমেনু (`main`)।
- ফুটারের তিনটি কলামের লিঙ্কসমূহ (`footer_director_services`, `footer_about_rick`, `footer_other`)।

### ৩. নতুন ব্লগ পোস্ট তৈরি বা এডিট করা
**ডিরেক্টরি:** `_posts/`
- ফরম্যাট: `YYYY-MM-DD-post-title.md` (যেমন: `2026-10-25-my-new-post.md`)
- পোস্টের শুরুতে ফ্রন্টম্যাটার (Front Matter):
  ```yaml
  ---
  layout: post
  title: "আপনার পোস্টের শিরোনাম"
  date: 2026-10-25 10:00:00 -0400
  author: "Rick Colosimo"
  permalink: /your-post-slug/
  excerpt: "পোস্টের সংক্ষিপ্ত বিবরণ..."
  categories:
    - five-minute-lawyer
  tags:
    - contracts
    - advice
  ---

  এখানে আপনার আর্টিকেলের মূল বক্তব্য Markdown ফরম্যাটে লিখুন।
  ```

### ৪. পেইজ তৈরি বা এডিট করা
**ডিরেক্টরি:** `_pages/`
- যেমন: `about.md`, `services.md`, `deals.md`, `tools.md`।
- ফ্রন্টম্যাটার:
  ```yaml
  ---
  layout: page
  title: "About Rick"
  permalink: /about/
  ---

  এখানে পেইজের কন্টেন্ট লিখুন।
  ```

### ৫. ইমেজ এবং ফাইল আপলোড করা
- নতুন ছবি বা ফাইল `assets/uploads/` ফোল্ডারে রাখুন।
- আর্টিকেলে ব্যবহার করতে লিখুন:
  ```markdown
  ![ছবির বিবরণ](/assets/uploads/your-image.png)
  ```

---

## লোকাল ডেভেলপমেন্ট ও বিল্ড কমান্ডস

### ১. ডিপেন্ডেন্সি ইনস্টল (প্রথমবার)
```bash
npm install
bundle install
```

### ২. Tailwind CSS কম্পাইল করা
```bash
npm run build:css
```

### ৩. সাইট রান ও লাইভ প্রিভিউ দেখা
```bash
bundle exec jekyll serve
```
ব্রাউজারে `http://localhost:4000` ওপেন করলেই সাইটটি দেখতে পাবেন।

### ৪. সম্পূর্ণ প্রোডাকশন বিল্ড
```bash
npm run build
```

---

## গিটহাব পেজে ডিপ্লয়মেন্ট (Deployment)

প্রোজেক্টটি গিটহাবে পুশ করলে স্বয়ংক্রিয়ভাবে GitHub Actions-এর মাধ্যমে কম্পাইল হয়ে GitHub Pages-এ লাইভ হয়ে যাবে।
```bash
git add .
git commit -m "Update site content"
git push origin main
```
