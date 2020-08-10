---
layout: article
category: voluntarios
date: 2020-07-23 16:45:00 -0000
title: ""
---

{% assign volunteers = site.data.volunteers %}

<table class="center" style="margin-left: auto; margin-right: auto;">
  <colgroup>
    <col width="45%" />
    <col width="5%" />
    <col width="50%" />
  </colgroup>
  <tbody>

    {% for data in volunteers %}
	{% assign volunteer = volunteers[data.first] %}

	    <tr>
	        <td style="text-align: right">{{ volunteer.role }}</td>
		
	        <td style="text-align: center">
		    {% if volunteer.contact == null %}
		        <!-- deixa em branco -->
		    {% else %}
		        {% if volunteer.contact_type == 'email' %}
		            <a href="mailto:{{ volunteer.contact }}" target="_blank"><i class="uil uil-envelope"></i></a>
		        {% endif %}
		        {% if volunteer.contact_type == 'linkedin' %}
		            <a href="https://{{ volunteer.contact }}" target="_blank"><i class="uil uil-linkedin"></i></a>
		        {% endif %}
		        {% if volunteer.contact_type == 'lattes' %}
		            <a href="https://{{ volunteer.contact }}" target="_blank"><i class="ai ai-lattes"></i></a>
		        {% endif %}
		        {% if volunteer.contact_type == 'insta' %}
		            <a href="https://{{ volunteer.contact }}" target="_blank"><i class="uil uil-instagram"></i></a>
		        {% endif %}
		        {% if volunteer.contact_type == 'web' %}
		            <a href="https://{{ volunteer.contact }}" target="_blank"><i class="uil uil-globe"></i></a>
		        {% endif %}
		    {% endif %}
		</td>

	        <td style="text-align: left">
		    {% if volunteer.link == null %}
		        {{ volunteer.name }}
		    {% else %}
		        <a href="https://{{ volunteer.link }}">{{ volunteer.name }}</a>
		    {% endif %}
	        </td>
	    </tr>

    {% endfor %}

  </tbody>
</table>
