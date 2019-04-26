---
layout: page
permalink: /sitemap/
title: "Sitemap"
excerpt: "An index of all the pages found on odayaka.vn, Nơi tổng hợp mọi liên kết, bài viết, thông tin đánh dấu trên Odayaka.vn"
---

Phân cấp và đánh dấu chỉ mục[^chimuc]. Dành cho các Robots của các cỗ máy tìm kiếm, hoặc Robots của riêng bạn, Odayaka có bản [XML version](/sitemap.xml) có sẵn để crawling nội dung.

[^chimuc]: **Chỉ mục**, **Mục lục** là việc đánh dấu tựa đề bài, đường dẫn tới những bài viết trên Odayaka.vn

<h2>Trang</h2>
<ul>
  <li><a href="/about/">Giới thiệu</a></li>
  <li><a href="/contact/">Địa chỉ và liên lạc</a></li>
  <li><a href="/faqs/">Giải đáp thắc mắc</a></li>
  <li><a href="/support/">Donate duy trì Odayaka</a></li>
  <li><a href="/tag/">Tag Lưu trữ</a></li>
  <li><a href="/terms/">Quy định thanh toán và vận chuyển</a></li>
</ul>

<h2><a href="/articles/">Bài viết từ Odayaka</a></h2>
<ul>
  {% for post in site.categories.articles %}
    {% include post-list.html %}
  {% endfor %}
</ul>

<h2><a href="/til/">Hôm nay tôi đã học được gì?</a></h2>
<ul>
  {% for post in site.categories.til %}
    {% include post-list.html %}
  {% endfor %}
</ul>

<h2><a href="/phuquoc-city/">Từ Phú Quốc</a></h2>
<ul>
  {% for post in site.categories.phuquoc-city %}
    {% include post-list.html %}
  {% endfor %}
</ul>

<h2><a href="/work/">Sản phẩm từ Odayaka</a></h2>
<ul>
  {% for post in site.work %}
    {% include post-list.html %}
  {% endfor %}
</ul>

{% include boilerplate/adsense-baiviet.md %}