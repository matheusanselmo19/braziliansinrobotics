---
layout: page
title: Timon2
subtitle: Agora
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


 Braços manipuladores estão cada vez mais presentes na dinâmica humana. No universo da produção automoblisitica, já é bastante comum notar a presença de robôs manipuladores exercecendo várias funções, principalmente como pintura e sodagem. Os manipualdores vem ganhando espaço em função de sual alta cpacidade de repetividade e  e da qualidade das opeções. Para garantir a repetividade, qualiade e além de ampliar a quantidade de aplicações, várias pesquisas e projetos estão sendo desenvolvido nos principais centro de pesquisa do mundo. 



O Projeto Timon2 tem por obejtivo realizar uma operação completamente autonona com o braço manipulador [JeRoTimon](https://braziliansinrobotics.com/project-jerotimon/), que foi desenvolvido em 2020 por um grupo de pesquisadores e especialista em robótica. A operação confere na busca e identificação de um marcador visual posicionado em uma caixa que está presente no ambiente, e após identificação, o robô deve pressionar o botão que também esta alocada na caixa. Esta operação ultizar plicações de **cinematica inversa**, que é crucial para a realização de operações autônomo com os braços manipuladores, **visão computacional** e **intregação de sistemas**.
 


## Um pouco sobre o Timon2
<p style="text-align: justify;">
  Timon2 foi inicializado em teve 18/02/2021 e deve ter sua finalização concluída em 17/03/2021. Este projet foi dividio em 5 etapas: Conceitual, Desgin, Simulação, Intregação e testes e conclusão. Estas etapas foram montando de acordo com Framework de projetos Robótica ultilizado pelo RASC e considerando as  principáis etapas que devem ser executadas para garantir o sucesso do projeto.
</p>


## Sistemas do Timon2
<p style="text-align: justify;">
Quase todo sistema robótico pode ser fracionado em conjuntos menores.  Timon2 foi divido  em 5 grupos: atuação, software, sensoriamento e alimentação. Esta fragemnetação ajuda a vizualização do robô diante de suas funcionalades e dos sues equpimantos. O Prototype strucre breakdown que apresenta da divisão do Timon2 em sistemas menores auxlia na vizualição dos equipamentos.  
</p>

<center>
<img src="{{ 'assets/img/timon2/pbs.png' | relative_url }}" width="800" text-align=center alt="ga" />
</center>

<p style="text-align: justify;">
  Durante a navegação, o robô deve encontrar obstáculos que podem dificultar a execução da missão. Para tratar os eventuais obstáculos serão implementados sensores que ajudarão na tarefa de evita-lós.
</p>
<p style="text-align: justify;">
  O sensor ultrassônico, implementado na parte frontal do robô, proverá informações da existência de obstáculos que podem estar a frente do robô.
  Enquanto um Lidar, juntamente com uma câmera de profundidade Mynteye serão utilizados para tornar este sistema robótico capaz de realizar a técnica SLAM, que irá permitir a construção do mapa e localização de forma simultânea.
</p>

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-3je9{background-color:#464646;border-color:#ffffff;color:#FFF;text-align:center;vertical-align:middle}
.tg .tg-7ogr{background-color:#464646;border-color:#ffffff;color:#ffffff;text-align:center;vertical-align:top}
.tg .tg-dbpp{background-color:#464646;border-color:#ffffff;color:#ffffff;text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-7ogr"><span style="font-weight:bold">Componentes</span><br></th>
    <th class="tg-7ogr"><span style="font-weight:bold">Modelo</span></th>
    <th class="tg-7ogr"><span style="font-weight:700;font-style:normal">Fabricante</span></th>
    <th class="tg-7ogr"><span style="font-weight:700;font-style:normal">Aplicação</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-dbpp"><img src="{{ 'assets/img/aperea/jetson_nano.png' | relative_url }}" width="100" alt="jetson" ></td>
    <td class="tg-3je9">Jetson Nano</td>
    <td class="tg-3je9">NVIDIA</td>
    <td class="tg-3je9">Unidade de processamento</td>
  </tr>
  <tr>
    <td class="tg-dbpp"><img src="{{ 'assets/img/aperea/cameraV2.png' | relative_url }}" width="100" alt="camerav2" ></td>
    <td class="tg-3je9">Câmera Module V2</td>
    <td class="tg-3je9">RaspberryPi</td>
    <td class="tg-3je9">Detectar a TAG e a esfera</td>
  </tr>
  <tr>
    <td class="tg-dbpp"><img src="{{ 'assets/img/aperea/mynteye.png' | relative_url }}" width="100" alt="mynteye"></td>
    <td class="tg-3je9">Câmera Stereo S1030</td>
    <td class="tg-3je9">Mynt eye</td>
    <td class="tg-3je9">Detectar obstáculos, localização e mapeamento</td>
  </tr>
  <tr>
    <td class="tg-dbpp"><img src="{{ 'assets/img/aperea/sensorultr.png' | relative_url }}" width="100" alt="sensorultr"></td>
    <td class="tg-3je9">Sensor Ultrassônico HC-SR04</td>
    <td class="tg-3je9">HC-SR04</td>
    <td class="tg-3je9">Detectar obstáculos</td>
  </tr>
  <tr>
    <td class="tg-dbpp"><img src="{{ 'assets/img/aperea/lidar.png' | relative_url }}" width="100" alt="lidar"></td>
    <td class="tg-3je9"><span style="font-weight:400;font-style:normal">Lidar LDS-01</span></td>
    <td class="tg-3je9">Robotis</td>
    <td class="tg-3je9">Mapeamento e localização</td>
  </tr>
  <tr>
    <td class="tg-dbpp"><img src="{{ 'assets/img/aperea/motordc.png' | relative_url }}" width="100" alt="motor"></td>
    <td class="tg-3je9">Motor DC 3-6v</td>
    <td class="tg-3je9">Rob</td>
    <td class="tg-3je9">Deslocamento</td>
  </tr>
</tbody>
</table>

<p style="text-align: justify;">
  A fim de identificar a TAG e a esfera colorida, a câmera V2 Raspberry Pi será utilizada para captar os dados visuais do ambiente. Os dados visuais serão processados com uso da biblioteca de visão computacional OpenCV.
</p>
<p style="text-align: justify;">
  Como mencionado anteriormente, o processamento dos dados que serão coletados pelos sensores será realizado pela placa Nvidia Jetson Nano. A placa conterá o sistema operacional Ubuntu 20.04, que permitirá a instalação da plataforma ROS, Robot Operation System, versão Noetic. 
</p>
<p style="text-align: justify;">
  Também será desenvolvido um sistema de gerenciamento de energia para monitorar a carga do sistema. A tabela acima apresenta mais informações com relação aos principais componentes que compõem o sistema do Aperea.
</p>
<br/>

<center>
  <h3 class="post-title">Equipe de desenvolvimento</h3><br/>
</center>
<div class="row">

<div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
<table class="table-borderless highlight">
<thead>
<tr>
<th><center><img src="{{ 'assets/img/people/juliana-1.png' | relative_url }}" width="100" alt="juliana" class="img-fluid rounded-circle" /></center></th>
<th></th>
<th><center><img src="{{ 'assets/img/people/matheusanselmo-1.png'| relative_url }}" width="100" alt="matheusanselmo" class="img-fluid rounded-circle"/></center></th>
<th></th>
<th><center><img src="{{ 'assets/img/people/marcoreis8b&w-1.png' | relative_url }}" width="100" alt="marco" class="img-fluid rounded-circle"/></center></th>
</tr>
</thead>
<tbody>
<tr class="font-weight-bolder" style="text-align: center margin-top: 0">
  <td width="33.33%">Juliana Santana</td>
  <td></td>
  <td width="33.33%">Matheus Anselmo</td>
  <td></td>
  <td width="33.33%">Marco Reis</td>
  </tr>
<tr style="text-align: center" >
<td style="vertical-align: top"><small>Pesquisadora Jr. do projeto <br>Engenheira Eletricista.</small></td>
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

### Resumo do Projeto
1. Categoria: 
2. Prazo: 04 meses
3. Data de início: <font color="#fbb117">10/maio/2021</font>
4. Data de término: <font color="#fbb117">20/agosto/2021</font>
5. Repositório URL: 
6. Sponsor: <a href="http://www.senaicimatec.com.br/en/"><font color="#fbb117">Senai CIMATEC</font></a>
7. Recursos materiais: US$
8. Apresentação URL:
9. Report URL: 
10. Artigos relacionados: 

<br>

##### Referência
1. <a href="https://jetbot.org/master"><font color="#fbb117">JETBOT</font></a>. Acesso em: 4 de Junho de 2021.



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
</div>