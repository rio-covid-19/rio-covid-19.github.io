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
		    {% if volunteer.e-mail != null %}
		        <a href="mailto:{{ volunteer.e-mail }}" target="_blank"><i class="uil uil-envelope"></i></a>
		    {% else %}
		        {% if volunteer.Linkedin != null %}
		            <a href="https://{{ volunteer.Linkedin }}" target="_blank"><i class="uil uil-linkedin"></i></a>
		        {% else %}
		            {% if volunteer.Lattes != null %}
		                <a href="https://{{ volunteer.Lattes }}" target="_blank"><i class="uil uil-lattes"></i></a>
		            {% else %}
		                {% if volunteer.Instagram != null %}
		                    <a href="https://{{ volunteer.Instagram }}" target="_blank"><i class="uil uil-instagram"></i></a>
		                {% else %}
		                    <!-- deixa em branco -->
		                {% endif %}
		            {% endif %}
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
