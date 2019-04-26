---
layout: page
permalink: /faqs/
title: "Câu hỏi và vấn đề thường gặp"
last_modified_at: 2018-02-19T09:56:45-05:00
excerpt: "Trong mọi trường hợp cần hỗ trợ, cách thức liên lạc nhanh gọn và đơn giản nhất là tiếp cận với Chăm sóc khách hàng Odayaka cho thuê xe Honda Phú Quốc đường dây nóng (24/24) 0899150055."
---

Trong mọi trường hợp cần hỗ trợ, cách thức liên lạc nhanh gọn và đơn giản nhất là tiếp cận với Chăm sóc khách hàng[^cskh] đường dây nóng 24/24 [**0899150055**](tel:+84-089-915-0055) (Phạm Xuân Tiếp). Hoặc tìm hiểu thêm các cách thức liên lạc trực tuyến Online khác (mạng xã hội, SMS, Zalo, Facebook) tại [**Liên lạc với Odayaka**](/contact/).

<div class="notice--warning" markdown="1">
Nếu du lịch vi vu tới Phú Quốc, bạn cần [Thuê xe Honda để tự do đi lại](/thuexe/) Hãy bấm vào liên kết đó và lựa chọn dòng xe phù hợp để thỏa thích vui chơi Phú Quốc như ở nhà, tự do, dễ dàng di chuyển, hoạt động cá nhân. 
</div>

[^cskh]: **Dịch vụ chăm sóc khách hàng** khi gặp sự cố, cần hỗ trợ gấp, xin quý khách gọi ngay tới 0899.150055 để được hỗ trợ trong thời gian nhanh nhất.


{% assign other_faqs = site.faqs | where: "type", "other" | sort: "order" %}
{% assign paper_faqs = site.faqs | where: "type", "paper" | sort: "order" %}

<ul>
{% for faq in other_faqs %}
<li><a href="{{ faq.url }}">{{ faq.title }}</a></li>
{% endfor %}
</ul>

## Vấn đề thanh toán, vận chuyển, nơi nhận, báo sự cố

<ul>
{% for faq in paper_faqs %}
<li><a href="{{ faq.url }}">{{ faq.title }}</a></li>
{% endfor %}
</ul>


{% include boilerplate/adsense-baiviet.md %}