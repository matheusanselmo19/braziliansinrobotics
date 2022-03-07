---
layout: page
title: Timon2
subtitle: Timon@Noetic
---
{% assign date_format = site.date_format | default: "%B %-d, %Y" %}
{%- capture site_tags -%}
    {%- for tag in site.tags -%}
      {% if tag contains 'timon2' %}
        {{- tag | first -}}{%- unless forloop.last -%},{%- endunless -%}
      {% endif %} 
    {%- endfor -%}
{%- endcapture -%}
{%- assign tags_list = site_tags | split:',' | sort -%}

<center><img src="{{ 'assets/img/timon2/timao.jpg' | relative_url }}" text-align=center width="500" alt="aperea" /><br></center>

<div class="before-content">
  <center>
    {%- for tag in tags_list -%}
      <br>
      <a href="#{{- tag -}}" class="btn btn-primary tag-btn"><i class="fas fa-tag" aria-hidden="true"></i>&nbsp;{{- tag -}}-posts&nbsp;({{site.tags[tag].size}})</a>
    {%- endfor -%}
  </center>    
  <!--hr class="mark"-->
</div>

 
Braços manipuladores estão cada vez mais presentes na dinâmica humana. No universo da produção automobilística, já é bastante comum notar a presença de robôs manipuladores exercendo várias funções, principalmente pintura e soldagem. Os manipuladores vem ganhando espaço em função de sua alta capacidade de repetitividade e da qualidade das operações. Para garantir a produtividade, qualidade e além de ampliar a quantidade de aplicações, várias pesquisas e projetos estão sendo desenvolvidos nos principais centros de pesquisa do mundo.



O Projeto Timon2 tem por objetivo realizar uma operação completamente autônoma com o braço manipulador [JeRoTimon](https://braziliansinrobotics.com/project-jerotimon/), que foi desenvolvido em 2020 por um grupo de pesquisadores e especialista em robótica. O JeRoTimon foi desenvolvido inicialmente para o ROS1 versão Melodic. A operação confere na busca e identificação de um marcador visual posicionado em uma caixa que está presente no ambiente, e após identificação, o robô deve pressionar o botão que também está alocado na caixa. Esta operação utiliza aplicações de **cinemática inversa**, que é crucial para a realização de operações autônomo com os braços manipuladores, **controle de trajetória e  posicionamento**, **visão computacional** e **integração de sistemas**.


## Um pouco sobre o Timon2


Timon2 foi inicializado em teve 18/02/2022. Este projeto foi dividido em 5 etapas: Conceitual, Design, Simulação, Integração e testes e conclusão. Estas etapas foram montadas de acordo com Framework de projetos Robótica utilizado pelo RASC e considerando as principais etapas que devem ser executadas para garantir o sucesso do projeto.



## Sistemas do Timon2

Quase todo sistema robótico pode ser fracionado em conjuntos menores.  Timon2 foi dividido  em 5 grupos: atuação, software, sensoriamento e alimentação. Esta fragmentação ajuda a visualização do robô diante de suas funcionalidades e dos sues equipamentos. O Prototype structure breakdown que apresenta a divisão do Timon2 em sistemas menores  e auxilia na visualização dos equipamentos.

<center>
<img src="{{ 'assets/img/timon2/pbs.png' | relative_url }}" width="800" text-align=center alt="ga" />
</center>

<br/>

O sistema mecânico é composto por 5 servomotores Dynamixel. Estes servomotores já possuem um controle de posição, trajetória e torque que foi implementado pelo seu desenvolvedor. O sistema de sensoriamento possui a câmera digital que será utilizada para detectar o marcador visual.
 
Os softwares que permitem a realização da cinemática inversa, controle de trajetória e posição do manipulador estão presentes no pacote  Moveit, numa versão é designada para o  ROS1 versão Noetic que foi projetado para o Ubuntu 20.04.  O pacote de software possui uma interface com as linguagens de programação C++ e Python,  o que permite o uso de programas desenvolvidos em ambas línguas para realizar interação com o manipulador. No atual projeto a interface com braço robótico será realizada usando a linguagem C ++. Para fornecer energia para o sistema será usado uma fonte 24V.




O desenvolvimento deste projeto envolve áreas importantes de grande importância para robótica, principalmente a industrial. Brevemente teremos alguns posts que demonstram a dinâmica das atividades que serão executadas para garantir o sucesso do projeto.


<br/>

<center>
  <h3 class="post-title">Equipe de desenvolvimento</h3><br/>
</center>
<div class="row">

<div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
<table class="table-borderless highlight">
<thead>
<tr>
<th><center><img src="{{ 'assets/img/people/mateusseixas-1.png' | relative_url }}" width="100" alt="juliana" class="img-fluid rounded-circle" /></center></th>
<th></th>
<th><center><img src="{{ 'assets/img/people/matheusanselmo-1.png'| relative_url }}" width="100" alt="matheusanselmo" class="img-fluid rounded-circle"/></center></th>
<th></th>
<th><center><img src="{{ 'assets/img/people/marcoreis8b&w-1.png' | relative_url }}" width="100" alt="marco" class="img-fluid rounded-circle"/></center></th>
</tr>
</thead>
<tbody>
<tr class="font-weight-bolder" style="text-align: center margin-top: 0">
  <td width="33.33%">Mateus Seixas</td>
  <td></td>
  <td width="33.33%">Matheus Anselmo</td>
  <td></td>
  <td width="33.33%">Marco Reis</td>
  </tr>
<tr style="text-align: center" >
<td style="vertical-align: top"><small>Pesquisador Jr. do projeto <br>Engenheiro Eletricista.</small></td>
<td></td>
<td style="vertical-align: top"><small>Pesquisador Jr. do projeto <br>Engenheiro de Controle e Automação.</small></td>
<td></td>
<td style="vertical-align: top"><small>Orientador do projeto <br>Mestre em Engenharia de Produção e Eng. Eletricista.</small></td>
</tr>
</tbody>
</table>
</div>
</div>





<br>
<hr class="mark">
<div id="full-tags-list">
<h3 class="post-title"><font color="#fbb117">Posts</font></h3>
  {%- for tag in tags_list -%}
      <h4 id="{{- tag -}}" class="linked-section">
          <i class="fas fa-tag" aria-hidden="true"></i>
          &nbsp;{{- tag -}}&nbsp;({{site.tags[tag].size}})
      </h4>
      <div class="post-list">
          {%- for post in site.tags[tag] -%}
              <div class="tag-entry">
                  <a href="{{ post.url | relative_url }}">{{- post.title -}}</a>
                  <div class="entry-date">
                      <time datetime="{{- post.date | date_to_xmlschema -}}">{{- post.date | date: date_format -}}</time>
                  </div>
              </div>
          {%- endfor -%}
      </div>
  {%- endfor -%}
</div>âmica da