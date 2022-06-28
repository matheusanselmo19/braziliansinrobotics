---
layout: page
title: PIRABOTS
subtitle: Autonomous Functionalities Implementation
---


<center><img src="{{ 'assets/img/pirabots/pirabots.png' | relative_url }}" alt="PIRABOTS" width="380"/></center>


Nos ROVs, praticamente todas as ações de movimentação e percepção do ambiente são executadas exclusivamente por operadores humanos. Operadores humanos tendem a ser mais suscetíveis a erros do que sistemas autônomos. A adaptação de algumas tarefa funcionalidade para uma responsabilidade de sistema autônomo deve aumentar a qualidade das operações e aliviar uma as ações do operador, já que este não será icunbido para todas as ações do veículo

Realização de implementação de funções autônomas nos veículos submarinos: Blue ROV e Bir-ROV. As ações que serão implementadas têm um foco inicial voltado para a execução da movimentação autônoma dos robôs. Os movimentos Surge, yaw e heave, que são os principais para navegação submersa, serão o s primeiros a serem desenvolvidos. Além do desenvolvimento do robô físico, será realizado simulações com objetivo de emular e testar as funcionalidades dos sistemas previamente da realização da aplicação do mundo real para obter o conhecimento sobre o comportamento  dos veículos

### Os veículos

O **BIR-ROV** é um ROV porte desenvolvido pelo por dois engenheiros robotisistas: [Frederico Oliveira](https://www.linkedin.com/in/frederico-goliveira/) e [Matheus Menezes](https://www.linkedin.com/in/mateussmenezes/). O BIR-ROV possui 6 thrusters para a realização das ações de movimentações.
<br>


<center><img src="{{ 'assets/img/pirabots/bir_rov.jpg' | relative_url }}" alt="PIRABOTS" width="380"/></center>



O **BlueROV2** é um famoso ROV desenvolvido pela companhia norte americana [Blue Robotics](https://bluerobotics.com/). Este veículo é  bastante usado em pesquisas, inspeções e monitoramentos de ambiente submarino. Assim como o BIR-ROV, O BlueROV2 possui 6 Thrusters para movimentação que permite  6 graus de liberdade. Seu Principal elemento de percepção é uma câmera digital, porém outros sensores podem ser aclopados.



<center><img src="{{ 'assets/img/pirabots/bluerov.png' | relative_url }}" alt="PIRABOTS" width="380"/></center>

<br>


### Principais Ferramentas

Para alcançar os objetivos, diversas ferramentas seram utilizadas durante a execução do projeto. O ROS é a principal framework que será usada para para a intregração dos sistemas. Para a simulação, O Gazebo será utilizado juntamente com ROS. Várias linguagem de programação serão utilizadas, C++ e Python devido bom seus interfaceamentos ROS teram usos relevantes. 

<br>

<center><img src="{{ 'assets/img/pirabots/tools.png' | relative_url }}" alt="PIRABOTS" width="880"/></center>

<br>




<center>
  <h3 class="post-title">Equipe de desenvolvimento</h3><br/>
</center>
<div class="row">
<br>

<br>
<div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
<table class="table-borderless highlight">
<thead>
<tr>
<th><center><img src="{{ 'assets/img/people/alexandreadonai-1.png' | relative_url }}" width="100" alt="alexandre" class="img-fluid rounded-circle" /></center></th>
<th></th>
<th><center><img src="{{ 'assets/img/people/matheusanselmo-1.png'| relative_url }}" width="100" alt="matheus" class="img-fluid rounded-circle"/></center></th>
<th></th>
<th><center><img src="{{ 'assets/img/people/marcoreis8b&w-1.png' | relative_url }}" width="100" alt="marco" class="img-fluid rounded-circle"/></center></th>
</tr>
</thead>
<tbody>
<tr class="font-weight-bolder" style="text-align: center margin-top: 0">
  <td width="33.33%">Alexandre Adonai</td>
  <td></td>
  <td width="33.33%">Matheus Anselmo</td>
  <td></td>
  <td width="33.33%">Marco Reis</td>
  </tr>
<tr style="text-align: center" >
<td style="vertical-align: top"><small>Pesquisadora Jr. do projeto <br>Graduando em Engenheira Eletricista.</small></td>
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