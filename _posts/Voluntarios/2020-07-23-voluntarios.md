---
layout: article
category: voluntarios
date: 2020-07-23 16:45:00 -0000
title: Nomes, cargos e descrições dos voluntários
---

<table class="Tabela-Voluntarios">
  <colgroup>
    <col width="40%" />
    <col width="30%" />
	<col width="10%" />
	<col width="20%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th style="text-align: left">Nome</th>
  <th style="text-align: left">Cargo</th>
  <th style="text-align: center">E-mail</th>
  <th style="text-align: center">Rede Social</th>
  </tr>
  </thead>
  <tbody>
    {% for order in (1..8) %}
        {% for volunteer in site.data.volunteer %}
	        {% capture volunteer_id %}{{ volunteer[0] | slice:0 }}{% endcapture %}
            {% capture volunteer_name %}{{ volunteer | first }}{% endcapture %}
	        {% assign each_volunteer = site.data.volunteer[volunteer_name] %}
	        {% if each_volunteer.Ordem == order %}
                <tr>
	                {% if each_volunteer.link == null %}
                        <td>{{each_volunteer.name}}</td>
		            {% else %}
                        <td><a href="{{ each_volunteer.link }}">{{ each_volunteer.name }}</a></td>
		            {% endif %}
					
					<td>{{each_volunteer.role}}</td>
					
					{% if each_volunteer.e-mail == null %}
		            {% else %}
						<td style="text-align: center"><a href="mailto:{{ each_volunteer.e-mail }}"><i class='uil uil-envelope' target="_blank"></i></a></td>
		            {% endif %}
					<td style="text-align: center">
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
        {% endfor %}
    {% endfor %}
  </tbody>
</table>