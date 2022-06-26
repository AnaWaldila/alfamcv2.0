# AlfaMCV Version 2.0

## Abstract

This is a software to calculate the behavior of the reinforced concrete beam subjected to a pontual load in the midpoint of the beam. Based on the physical-geometric characteristics of the structure, AlfaMCV is able to calculate some pieces of information about the structure, considering linear and non-linear behavior of the concrete in this stress-strain graph. In other words, this case presents the real behavior of the structure. Now, it is considered the T beam's section.
AlfaMCV is able to present some pieces of information about the structure, such as: neutral axis for the analysis of each step, stresses and strain in steel and concrete (in both cases, compression and tension), moment in the midpoint of the beam and its deflection.
Finally, the user can export the table to Excel software and create their own analyzes and graphs.

## Introduction

Concrete is a weak material whose structure is calculated without the tensile behavior in concrete, i.e., only compression in concrete is considered. For the case of steel, both cases are considered compression and tension. In this region, Figure 1 shows the areas of all stresses on concrete and steel.

<div>
<img src="Figures/Concrete_Graph.png" width="30%">
</div>
<p>
 <b>Figure 1:</b> Stress - Strain Concrete Configuration (Reis et al, 2017). 
</p>

Where A<sub>st</sub> is steel area in tension, F<sub>st</sub> is steel's force in tension, <i>&epsilon;</i><sub>cm</sub> is compression's strain in concrete, F<sub>cm</sub> is compression's force in concrete, k<sub>d</sub> is neutral axis and M<sub>k</sub> is characteristics moment.

It is already well known about the compressive behavior of concrete, according to BAZANT (1984) and PFEIL (1969) presented in the literature. In addition, this type of behavior (the parabolic rectangular diagram) has been used by NBR 6118:2014, as shown in Figure 2.

<div>
<img src="Figures/Concrete_ABNT.png" width="40%">
</div>
<p>
 <b>Figure 2:</b> Stress - Strain Concrete Configuration in ABNT NBR 6118:2014 
</p>

Where f<sub>ck</sub> is the characteristic concrete compression resistence, f<sub>cd</sub> is the calculated concrete compression resistence, <i>&epsilon;</i><sub>c2</sub> is strain when concrete starts the plastic deformation and <i>&epsilon;</i><sub>cu</sub> is strain when concrete ruptures.

However, the tension behavior in concrete is not used in design structures and the studies by BAZANT (1984) showed that this area can contribute to the evolution of the general stiffness of the structure, as in Figure 3.

<div>
<img src="Figures/Concrete_Tension.png" width="30%">
</div>
<p>
 <b>Figure 3:</b> Stress - Strain Concrete Configuration in Tension (Reis et al, 2017)
</p>

Where f<sub>tk</sub> is characteristic concrete tension resistence, <i>&epsilon;</i><sub>tp</sub> is concrete strain in maximun concrete tension resistence, E<sub>c</sub> is Moduli's Young, <i>&epsilon;</i><sub>tf</sub> is concrete strain when tension stress is zero and E<sub>t</sub> is tangent Modulus.

## Methodology

All methodology can see in REIS et al (2017), BAZANT (1984) and Cavalcante et al. (2021)

## About the Software

AlfaMCV (Moment Curvature in Reinforced Concrete Beams or Momento Curvatura em Vigass de Concreto Armado, in Portuguese), is a simple software which can interact the user, i.e., it is a GUI interface. The software was developed with the Visual Basic computational programing and the Microsoft Visual Studio 2017 platform was used. The software is in Portuguese. AlfaMCV presents a main window which four buttons are presented: "Calcular" (Calculation), "Sobre o Software" (About the Software), "Ajuda" (Help0 and "Sair" (Exit), as shown in Figure 4.

<div>
<img src="Figures/Alfa_Principal.png" width="40%">
</div>
<p>
 <b>Figure 4:</b> AlfaMCV - Principal Window 
</p>

The "Calcular" button opens a new window, where the user can inpput data about the physical-geometric characteristics of the structure. The user needs: 
* Choose between "Seção Retangular" (rectangular section) or "Seção T" (T section);
* "Altura Total - H (cm)" (web H, cm);
* "Altura Mesa - Hs (cm)" (flange thickness);
* "Largura - B (cm)" (flange B, cm); 
* "Largura - B<sub>w</sub> (cm)" (web thickness, cm); 
* "Vão (cm)" (beam length, cm); 
* "Altura útil total - d (cm)" (total useful height d, cm); 
* "Resistência à Compressão do Concreto - f<sub>ck</sub> (MPa)" (concrete compressive strength - f<sub>ck</sub> MPa); 
* "Resistência à Tração do Concreto - f<sub>tk</sub> (MPa)" (tensile strength of concrete f<sub>ck</sub> MPa); 
* "Módulo de Elasticidade do Concreto (MPa)" (Concrete's Young Modulus MPa); 
* "Área de Aço de Compressão - A'<sub>s</sub> (cm²)" (Steel Compression Area A'<sub>s</sub>, cm²); 
* "Área de aço de Tração - A<sub>s</sub> (cm²)" (strength area of steel A<sub>s</sub>, cm²); 
* "Steel Elasticity Modulus - E<sub>s</sub> (MPa)" (Young Modulus MPa steel);
* "Escoamento Aço - f<sub>y</sub> (MPa)" (f<sub>y</sub> MPa yield steel). 
All these features can be seen in Figure 5.

<div>
<img src="Figures/Alfa_Calculus.png" width="60%">
</div>
<p>
 <b>Figure 5:</b> AlfaMCV - Calculus Window 
</p>

After intput the data, a new window opens with all the pieces of information about the structure. The first tab "Regime Linear" (Linear Behavior) presents some information about the structure, such as "Altura da linha neutra (cm)" (Height of the neutral axis, cm), "Deformação máxima de tração do concreto" (maximum strain of concrete in tensile behavior), "Deformação do concreto na compressão quando a tensão máxima é obtido" (Concrete strain in compression when maximum stress is obtained), "Deformação máxima de compressão do concreto" (maximum compressive strain of concrete), "Deformação de tração do aço" (Tensile strain of steel), "Deformação de compressão do aço" (Compressive strain of steel), "Momento de fissuração (kN.m)" (Cracking moment (kN. m)). All these features is shown Figure 6.

<div>
<img src="Figures/Alfa_Results1.png" width="60%">
</div>
<p>
 <b>Figure 6:</b> AlfaMCV - Result Window - Linear Behavior
</p>

The "Regime Não Linear" (Nonlinear Behavior) tab presents the behavior of a structure for each step of the analysis. Thus, in this case, there are 8 columns with information about the structure: "Índice i" (index i), "Tipo de Regime" (type of behavior), "Linha Neutra (cm)" (neutral axis, cm), "Deformação Compressão Concreto" (concrete compression strain), "Deformação Compressão do Aço" (steel compression strain), "Deformação Tração do Aço" (steel tension strain), "Momento (kN.m)" (Moment kN.m) and "Deflexão (cm)" (deflexion, cm). This table is shown in Figure 7.

<div>
<img src="Figures/Alfa_Results2.png" width="60%">
</div>
<p>
 <b>Figure 7:</b> AlfaMCV - Result Window - Nonlinear Behavior
</p>

After that, the user can export this table to the Excel software, just press the button "Exportar para Excel" (export to excel) on the menu and rename the file and save it anywhere on the computer. The second button on the menu, "Ajuda" (Help), opens a window with some instructions on how the user can use the software, input data and output data, as shown in Figure 8.

<div>
<img src="Figures/Alfa_Help.png" width="60%">
</div>
<p>
 <b>Figure 8:</b> AlfaMCV - Help Window - Nonlinear Behavior
</p>

Finally, the third button is about the software, i.e., some pieces of information about the developer, professors and the University. Figure 9 shows this description.

<div>
<img src="Figures/Alfa_About.png" width="60%">
</div>
<p>
 <b>Figure 9:</b> AlfaMCV - About Window - Nonlinear Behavior
</p>

The AlfaMCV software has a Brazilian Registration at the INPI (National Institute of Industrial Property) and the registration number is BR 51 2016 001434-2.

## Results

Some analysis was realized with differents considerations of steel area in concrete section. Next, a table with physics-geometric characteristics:

<div>
<img src="Figures/Result_Table.png" width="40%">
</div>
<p>
 <b>Figure 10:</b> Structure Physics-Geometric Characteristics
</p>


### Reinforced Concrete with normal reinforcement

For this case was considered the rate between neutral axis and useful height (<i>&sci;</i>) = 0.2593, M<sub>k</sub> = 1652.53 kN.m and a steel area with A<sub>sc</sub> = 48.075 cm². The graphic was ploted, Figure 11, and all results have been compared: models of BAZANT (1984) and SAENZ (1964) considering the tension in concrete (blue line) and the moment of rupture (blue line). It is possible to see that all cases converge to approximately the same moment value, M<sub>k</sub> = 1678.04 kN.m. The deflection shows by the software (in linear behavior) is 0.008241 cm and calculated by literature is 0.01109 cm.

<div>
<img src="Figures/Result_NR.png" width="60%">
</div>
<p>
 <b>Figure 11:</b> Reinforced Concrete with normal reinforcement
</p>

### Reinforced Concrete with hight reinforcement

For this case was considered the rate between neutral axis and useful height (<i>&sci;</i>) = 0.6283, M<sub>k</sub> = 2327.53 kN.m and a steel area with A<sub>sc</sub> = 76.76 cm². The graphic was ploted, Figure 12, and all results have been compared: models of BAZANT (1984) and SAENZ (1964) considering the tension in concrete (blue line) and the moment of rupture (blue line). It is possible to see that all cases converge to approximately the same moment value, M<sub>k</sub> = 2459.63 kN.m. The deflection shows by the software (in linear behavior) is 0.008758 cm and calculated by literature is 0.00876 cm.

<div>
<img src="Figures/Result_HR.png" width="60%">
</div>
<p>
 <b>Figure 12:</b> Reinforced Concrete with hight reinforcement
</p>

### Reinforced Concrete with compression and tension reinforcement

For this case was considered M<sub>k</sub> = 2500 kN.m and a steel area with A<sub>sc</sub> = 17.35 cm² and A<sub>st</sub> = 81.69 cm². The graphic was ploted, Figure 13, and all results have been compared: models of BAZANT (1984) and SAENZ (1964) considering the tension in concrete (blue line) and the moment of rupture (blue line). It is possible to see that all cases converge to approximately the same moment value, M<sub>k</sub> = 2761.82 kN.m. The deflection shows by the software (in linear behavior) is 0.008551491 cm and calculated by literature is 0.00855 cm.

<div>
<img src="Figures/Result_DR.png" width="60%">
</div>
<p>
 <b>Figure 13:</b> Reinforced Concrete with compression and tension reinforcement
</p>

## References

Cavalcante, T.M.; Ramos, T.C.B., Reis, A.W.Q.R., Burgos, R.B. Implementação do Software AlfaMCV com Base no Comportamento de Vigas de Concreto Armado com Seção T. In: Caderno especial dos melhores artigos do 62º Congresso Brasileiro do Concreto, 2021.

Reis, A.W.Q.R., Burgos, R.B, Magalhães, M.S. Development of a software for the numerical modeling of reinforced concrete sections. 3° EMI International Conference, 2017.

Reis, A.W.Q.R., Burgos, R.B, Magalhães, M.S. Desenvolvimento de um programa computacional para obtenção de gráficos momento vs curvatura e momento vs deflexão em vigas de concreto armado. 59° Congresso Brasileiro do Concreto, 2017.

Reis, A.W.Q.R., Burgos, R.B, Magalhães, M.S. Development of a software for the numerical modeling of reinforced concrete sections - AlfaMCV. SoftwareX - Elsevier, 2020.

Reis, A.W.Q.R. Modelagem Numerica de Seções de Concreto Armado. Rio de Janeiro State University. Graduation Thesis, 2017.

## Information About the Software

Rio de Janeiro State University

Faculty of Engineering

Developers: Thaís Macedo Cavalcanti, Túlio Costa Batista Ramos and Ana Waldila de Queiroz Ramiro Reis

Professors: Margareth da Silva Magalhães and Rodrigo Bird Burgos

Contact: anawaldila@hotmail.com
