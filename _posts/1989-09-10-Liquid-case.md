---
layout: post
title: Liquid-case
tags: Liquid
categories: Jekyll
---

## Case 语句
适用于当条件实例很多的情况。
\~\~
{% raw %}
{% case template %}
{% when 'label' %}
	 // {{ label.title }}
{% when 'product' %}
	 // {{ product.vendor | link_to_vendor }} / {{ product.title }}
{% else %}
	 // {{page_title}}
{% endcase %}
{% endraw %}
\~\~\~
{: .language-ruby}