---
layout: article
category: voluntarios
date: 2020-07-23 16:45:00 -0000
title: "  "
---

{% assign volunteers = site.data.volunteer %}

<table class="Tabela-Organização">
  <colgroup>
    <col width="420px" />
    <col width="20px" />
	<col width="250px" />
	<col width="150px" />
  </colgroup>
  <tbody>
    <tr class="header text-uppercase">
	<th colspan=4 height="50px">Comitê organizador</th>
    </tr>
    <tr></tr> <!-- espaço em branco -->
    
    {% for data in volunteers %}
	{% assign volunteer = volunteers[data.first] %}

	{% if volunteer.grupo == "organizacao" %}
	    <tr>
	        <td style="text-align: right">{{ volunteer.role }}</td>
		
		<td style="text-align: center"></td>
		{% if volunteer.link == null %}
		    <td style="text-align: left">{{ volunteer.name }}</td>
		{% else %}
		    <td style="text-align: left"><a href="https://{{ volunteer.link }}">{{ volunteer.name }}</a></td>
		{% endif %}
		
		<td style="text-align: left">
		    {% if volunteer.e-mail == null %}
		    {% else %}
		        <a href="mailto:{{ volunteer.e-mail }}" target="_blank"><i class="uil uil-envelope"></i></a>
		    {% endif %}
		    {% if volunteer.Instagram == null %}
		    {% else %}
		        <a href="https://{{ volunteer.Instagram }}" target="_blank"><i class="uil uil-instagram"></i></a>
		    {% endif %}
		    {% if volunteer.Linkedin == null %}
		    {% else %}
		        <a href="https://{{ volunteer.Linkedin }}" target="_blank"><i class="uil uil-linkedin"></i></a>
		    {% endif %}
		</td>
	    </tr>
	{% endif %}

    {% endfor %}

    <tr></tr> <!-- espaço em branco -->

    <tr class="header text-uppercase">
        <th colspan=4 height="50px">Equipe administrativa</th>
    </tr>
    <tr></tr> <!-- espaço em branco -->
    
    {% for data in volunteers %}
	{% assign volunteer = volunteers[data.first] %}

	{% if volunteer.grupo == "admin" %}
	    <tr>
	        <td style="text-align: right">{{ volunteer.role }}</td>
		
		<td style="text-align: center"></td>
		{% if volunteer.link == null %}
		    <td style="text-align: left">{{ volunteer.name }}</td>
		{% else %}
		    <td style="text-align: left"><a href="https://{{ volunteer.link }}">{{ volunteer.name }}</a></td>
		{% endif %}
		
		<td style="text-align: left">
		    {% if volunteer.e-mail == null %}
		    {% else %}
		        <a href="mailto:{{ volunteer.e-mail }}" target="_blank"><i class="uil uil-envelope"></i></a>
		    {% endif %}
		    {% if volunteer.Instagram == null %}
		    {% else %}
		        <a href="https://{{ volunteer.Instagram }}" target="_blank"><i class="uil uil-instagram"></i></a>
		    {% endif %}
		    {% if volunteer.Linkedin == null %}
		    {% else %}
		        <a href="https://{{ volunteer.Linkedin }}" target="_blank"><i class="uil uil-linkedin"></i></a>
		    {% endif %}
		</td>
	    </tr>
	{% endif %}

    {% endfor %}

    <tr></tr> <!-- espaço em branco -->

    <tr class="header text-uppercase">
        <th colspan=4 height="50px">Equipe de manutenção</th>
    </tr>
    <tr></tr> <!-- espaço em branco -->
    
    {% for data in volunteers %}
	{% assign volunteer = volunteers[data.first] %}

	{% if volunteer.grupo == "tecnico" %}
	    <tr>
	        <td style="text-align: right">{{ volunteer.role }}</td>
		
		<td style="text-align: center"></td>
		{% if volunteer.link == null %}
		    <td style="text-align: left">{{ volunteer.name }}</td>
		{% else %}
		    <td style="text-align: left"><a href="https://{{ volunteer.link }}">{{ volunteer.name }}</a></td>
		{% endif %}
		
		<td style="text-align: left">
		    {% if volunteer.e-mail == null %}
		    {% else %}
		        <a href="mailto:{{ volunteer.e-mail }}" target="_blank"><i class="uil uil-envelope"></i></a>
		    {% endif %}
		    {% if volunteer.Instagram == null %}
		    {% else %}
		        <a href="https://{{ volunteer.Instagram }}" target="_blank"><i class="uil uil-instagram"></i></a>
		    {% endif %}
		    {% if volunteer.Linkedin == null %}
		    {% else %}
		        <a href="https://{{ volunteer.Linkedin }}" target="_blank"><i class="uil uil-linkedin"></i></a>
		    {% endif %}
		</td>
	    </tr>
	{% endif %}

    {% endfor %}

  </tbody>
</table>
