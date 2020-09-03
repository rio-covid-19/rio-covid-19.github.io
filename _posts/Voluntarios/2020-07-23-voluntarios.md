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
	
	{% for equipe in (1..2) %}
	<tr> <th style="text-align: center" colspan=3></th> </tr>
	<tr> <th style="text-align: center" colspan=3></th> </tr>
	<tr> <th style="text-align: center" colspan=3></th> </tr>
	<tr> <th style="text-align: center" colspan=3></th> </tr>
		{% if equipe == 1 %}
			{% assign Grupo = 'NRVM' %}
			<tr> <th style="text-align: center" colspan=3><h5>Equipe do Núcleo de Reparos de Ventiladores Mecânicos (NRVM)</h5></th> </tr>
		{% else if equipe == 2 %}
			{% assign Grupo = 'EAVM' %}
			<tr> <th style="text-align: center" colspan=3><h5>Equipe do Projeto "Engineers Assisting Ventilator Maintenance" (EAVM)</h5></th> </tr>
		{% endif %}
		<tr> <th style="text-align: center" colspan=3></th> </tr>
		<tr> <th style="text-align: center" colspan=3></th> </tr>
		<tr> <th style="text-align: center" colspan=3></th> </tr>
		<tr> <th style="text-align: center" colspan=3></th> </tr>
	    {% for order in (1..6) %}
		{% assign flag = 0 %}
            {% for data in volunteers %}
	            {% assign volunteer = volunteers[data.first] %}
                {% if volunteer.ordem == order and volunteer.grupo == Grupo%}
	                 <tr>
					     <td style="text-align: right">
					     {% if flag == 0 %}
	                         {{ volunteer.role }}
							 {% assign flag = 1 %}
						 {% endif %}
						 </td>
							  
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
	    		{% endif %}
            {% endfor %}
        {% endfor %}
	{% endfor %}

  </tbody>
</table>
