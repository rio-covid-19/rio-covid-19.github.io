---
layout: article
category: voluntarios
date: 2020-07-23 16:45:00 -0000
title: "  "
---
<table class="Tabela-Organização">
  <colgroup>
    <col width="420px" />
    <col width="20px" />
	<col width="250px" />
	<col width="150px" />
  </colgroup>
   <tbody>
   <tr class="header">
   <th colspan=4 height="50px">ORGANIZAÇÃO </th>
   </tr>
   <tr>
   <th colspan=4>     </th>
   </tr>
    {% for order in (1..3) %}
        {% for volunteer in site.data.volunteer %}
	        {% capture volunteer_id %}{{ volunteer[0] | slice:0 }}{% endcapture %}
            {% capture volunteer_name %}{{ volunteer | first }}{% endcapture %}
	        {% assign each_volunteer = site.data.volunteer[volunteer_name] %}
			{% if each_volunteer.grupo == "organizacao" %}
	        {% if each_volunteer.Ordem == order %}
			    <tr>		
					<td style="text-align: right">{{each_volunteer.role}}</td>
					<td style="text-align: center"></td>
					{% if each_volunteer.link == null %}
                        <td style="text-align: left">{{each_volunteer.name}}</td>
		            {% else %}
                        <td style="text-align: left"><a href="{{ each_volunteer.link }}">{{ each_volunteer.name }}</a></td>
		            {% endif %}
					<td style="text-align: left">
					{% if each_volunteer.e-mail == null %}
                    {% else %}
                        <a href="mailto:{{ each_volunteer.e-mail }}"><i class='uil uil-envelope' target="_blank"></i></a>
                    {% endif %}
				    {% if each_volunteer.Instagram == null %}
		            {% else %}
                        <a href="http://{{each_volunteer.Instagram}}" target="_blank"><i class='uil uil-instagram'></i></a>
		            {% endif %}
					{% if each_volunteer.Linkedin == null %}
                    {% else %}
                        <a href="http://{{each_volunteer.Linkedin}}" target="_blank"><i class='uil uil-linkedin' target="_blank"></i></a>
                    {% endif %}
					</td>
                </tr>
            {% endif %}
			{% endif %}
        {% endfor %}
    {% endfor %}
	<tr></tr>
   <tr class="header">
   <th colspan=4 height="50px">SUPORTE ADMINISTRATIVO</th>
   </tr>
   <tr></tr>
    {% for order in (1..4) %}
        {% for volunteer in site.data.volunteer %}
	        {% capture volunteer_id %}{{ volunteer[0] | slice:0 }}{% endcapture %}
            {% capture volunteer_name %}{{ volunteer | first }}{% endcapture %}
	        {% assign each_volunteer = site.data.volunteer[volunteer_name] %}
			{% if each_volunteer.grupo == "admin" %}
	        {% if each_volunteer.Ordem == order %}
                <tr>		
					<td style="text-align: right">{{each_volunteer.role}}</td>
					<td style="text-align: center"></td>
					{% if each_volunteer.link == null %}
                        <td style="text-align: left">{{each_volunteer.name}}</td>
		            {% else %}
                        <td style="text-align: left"><a href="{{ each_volunteer.link }}">{{ each_volunteer.name }}</a></td>
		            {% endif %}
					<td style="text-align: left">
					{% if each_volunteer.e-mail == null %}
                    {% else %}
                        <a href="mailto:{{ each_volunteer.e-mail }}"><i class='uil uil-envelope' target="_blank"></i></a>
                    {% endif %}
				    {% if each_volunteer.Instagram == null %}
		            {% else %}
                        <a href="http://{{each_volunteer.Instagram}}" target="_blank"><i class='uil uil-instagram'></i></a>
		            {% endif %}
					{% if each_volunteer.Linkedin == null %}
                    {% else %}
                        <a href="http://{{each_volunteer.Linkedin}}" target="_blank"><i class='uil uil-linkedin' target="_blank"></i></a>
                    {% endif %}
					</td>
                </tr>
            {% endif %}
			{% endif %}
        {% endfor %}
    {% endfor %}
	<tr></tr>
   <tr class="header">
   <th colspan=4 height="50px">SUPORTE TÉCNICO PARA MANUTENÇÃO </th>
   </tr>
   <tr></tr>
    {% for order in (1..2) %}
        {% for volunteer in site.data.volunteer %}
	        {% capture volunteer_id %}{{ volunteer[0] | slice:0 }}{% endcapture %}
            {% capture volunteer_name %}{{ volunteer | first }}{% endcapture %}
	        {% assign each_volunteer = site.data.volunteer[volunteer_name] %}
			{% if each_volunteer.grupo == "tecnico" %}
	        {% if each_volunteer.Ordem == order %}
                <tr>		
					<td style="text-align: right">{{each_volunteer.role}}</td>
					<td style="text-align: center"></td>
					{% if each_volunteer.link == null %}
                        <td style="text-align: left">{{each_volunteer.name}}</td>
		            {% else %}
                        <td style="text-align: left"><a href="{{ each_volunteer.link }}">{{ each_volunteer.name }}</a></td>
		            {% endif %}
					<td style="text-align: left">
					{% if each_volunteer.e-mail == null %}
                    {% else %}
                        <a href="mailto:{{ each_volunteer.e-mail }}"><i class='uil uil-envelope' target="_blank"></i></a>
                    {% endif %}
				    {% if each_volunteer.Instagram == null %}
		            {% else %}
                        <a href="http://{{each_volunteer.Instagram}}" target="_blank"><i class='uil uil-instagram'></i></a>
		            {% endif %}
					{% if each_volunteer.Linkedin == null %}
                    {% else %}
                        <a href="http://{{each_volunteer.Linkedin}}" target="_blank"><i class='uil uil-linkedin' target="_blank"></i></a>
                    {% endif %}
					</td>
                </tr>
            {% endif %}
			{% endif %}
        {% endfor %}
    {% endfor %}
	<tr></tr>
   <tr class="header">
   <th colspan=4 height="50px"> MARKETING </th>
   </tr>
   <tr></tr>
    {% for order in (1..2) %}
        {% for volunteer in site.data.volunteer %}
	        {% capture volunteer_id %}{{ volunteer[0] | slice:0 }}{% endcapture %}
            {% capture volunteer_name %}{{ volunteer | first }}{% endcapture %}
	        {% assign each_volunteer = site.data.volunteer[volunteer_name] %}
			{% if each_volunteer.grupo == "mkt" %}
	        {% if each_volunteer.Ordem == order %}
                <tr>		
					<td style="text-align: right">{{each_volunteer.role}}</td>
					<td style="text-align: center"></td>
					{% if each_volunteer.link == null %}
                        <td style="text-align: left">{{each_volunteer.name}}</td>
		            {% else %}
                        <td style="text-align: left"><a href="{{ each_volunteer.link }}">{{ each_volunteer.name }}</a></td>
		            {% endif %}
					<td style="text-align: left">
					{% if each_volunteer.e-mail == null %}
                    {% else %}
                        <a href="mailto:{{ each_volunteer.e-mail }}"><i class='uil uil-envelope' target="_blank"></i></a>
                    {% endif %}
				    {% if each_volunteer.Instagram == null %}
		            {% else %}
                        <a href="http://{{each_volunteer.Instagram}}" target="_blank"><i class='uil uil-instagram'></i></a>
		            {% endif %}
					{% if each_volunteer.Linkedin == null %}
                    {% else %}
                        <a href="http://{{each_volunteer.Linkedin}}" target="_blank"><i class='uil uil-linkedin' target="_blank"></i></a>
                    {% endif %}
					</td>
                </tr>
            {% endif %}
			{% endif %}
        {% endfor %}
    {% endfor %}
  </tbody>
</table>
