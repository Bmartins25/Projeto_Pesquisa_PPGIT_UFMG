# Projeto_Pesquisa_PPGIT_UFMG

Aluno: Bruno Martins Bartolomeu

Tema: Avaliação e Conformidade de Modelos de IA responsável em Saúde

https://physionet.org/content/mimiciv/3.1/

Base de dados: MIMIC-IV 

Linguagem: Python

---

Resumo

Dados médicos coletados retrospectivamente têm a oportunidade de aprimorar o atendimento ao paciente por meio da descoberta de conhecimento e do desenvolvimento de algoritmos. A ampla reutilização de dados médicos é desejável para o bem público, mas o compartilhamento de dados deve ser feito de forma a proteger a privacidade do paciente. Aqui, apresentamos o Medical Information Mart for Intensive Care (MIMIC)-IV, um grande conjunto de dados desidentificados de pacientes internados no departamento de emergência ou em uma unidade de terapia intensiva no Beth Israel Deaconess Medical Center em Boston, Massachusetts. O MIMIC-IV contém dados de mais de 65.000 pacientes internados em uma UTI e mais de 200.000 pacientes internados no departamento de emergência. O MIMIC-IV incorpora dados contemporâneos e adota uma abordagem modular para a organização de dados, destacando a procedência dos dados e facilitando o uso individual e combinado de fontes de dados distintas. O MIMIC-IV pretende dar continuidade ao sucesso do MIMIC-III e oferecer suporte a um amplo conjunto de aplicações na área da saúde.

---

Fundo

Nos últimos anos, houve um movimento coordenado em direção à adoção de sistemas de registros médicos digitais em hospitais. Nos EUA, quase 96% dos hospitais tinham um sistema de registro eletrônico de saúde digital (EHR) em 2015 [1]. Dados médicos coletados retrospectivamente têm sido cada vez mais usados para epidemiologia e modelagem preditiva. Esta última se deve, em parte, à eficácia das abordagens de modelagem em grandes conjuntos de dados [2]. Apesar desses avanços, o acesso a dados médicos para melhorar o atendimento ao paciente continua sendo um desafio significativo. Embora os motivos para o compartilhamento limitado de dados médicos sejam multifacetados, as preocupações com a privacidade do paciente são destacadas como uma das questões mais significativas. Embora estudos com pacientes tenham demonstrado um consenso quase uniforme de que dados médicos desidentificados devem ser usados para melhorar a prática médica, especialistas na área continuam a debater os mecanismos ideais para fazê-lo. Excepcionalmente, o banco de dados MIMIC-III adotou um esquema de acesso permissivo que permitiu ampla reutilização dos dados [3]. Esse mecanismo tem se mostrado bem-sucedido no amplo uso do MIMIC-III em uma variedade de estudos, desde a avaliação da eficácia do tratamento em coortes bem definidas até a previsão de desfechos-chave para os pacientes, como a mortalidade. O MIMIC-IV visa dar continuidade ao sucesso do MIMIC-III, com uma série de alterações para melhorar a usabilidade dos dados e permitir mais aplicações em pesquisas.

---

Notas de lançamento

MIMIC-IV v3.1

O MIMIC-IV v3.1 foi lançado em outubro de 2024. Esta versão corrigiu pequenos bugs relatados pela comunidade:

Os itemidvalores nas tabelas d_labitems e labevents foram alterados para um subconjunto de medições laboratoriais entre as versões 2.2 e 3.0. Essa alteração não foi intencional. As tabelas foram atualizadas e os valores d_labitems e labevents itemid foram verificados para serem consistentes com a versão 2.2.
Dois subject_idestavam presentes em várias tabelas de dados, mas não na tabela de pacientes . Esses indivíduos foram removidos das tabelas de dados. As restrições do banco de dados com uma chave estrangeira para a subject_id coluna na tabela de pacientes agora devem funcionar corretamente.
Se estiver atualizando da v3.0, observe que somente as seguintes tabelas foram modificadas (e, portanto, requerem atualização):

* d_labitems
* diagnósticos_icd
* códigos drg
* eventos de laboratório
* eventos de microbiologia
* OMR
* transferências
* icustays

---

Referências

Henry, J., Pylypchuk, Y., Searcy T. & Patel V. (maio de 2016). Adoção de Sistemas de Registro Eletrônico de Saúde entre Hospitais Não Federais de Cuidados Agudos dos EUA: 2008-2015. Resumo de Dados do ONC, nº 35. Escritório do Coordenador Nacional de Tecnologia da Informação em Saúde: Washington, DC.
Halevy, A., Norvig, P., & Pereira, F. (2009). A eficácia irracional dos dados. IEEE Intelligent Systems, 24(2), 8-12.
Johnson, AE, Pollard, TJ, Shen, L., Lehman, LH, Feng, M., Ghassemi, M., ... e Mark, RG (2016). MIMIC-III, um banco de dados de cuidados intensivos de livre acesso. Dados científicos, 3(1), 1-9.
Documentação online do MIMIC. https://mimic.mit.edu
Johnson AE, Stone DJ, Celi LA, Pollard TJ. O Repositório de Códigos MIMIC: possibilitando a reprodutibilidade na pesquisa em terapia intensiva. Journal of the American Medical Informatics Association. 2018 jan;25(1):32-9.
Alistair Johnson, Tom Pollard, Jim Blundell, Brian Gow, Erinhong, Nicolas Paris e outros. MIT-LCP/código-mimic: Código MIMIC v2.1.1. Zenodo; 2021. https://doi.org/10.5281/zenodo.821871
Johnson, A., Pollard, T., Horng, S., Celi, LA, & Mark, R. (2023). MIMIC-IV-Note: Notas clínicas de texto livre desidentificadas (versão 2.2). PhysioNet. https://doi.org/10.13026/1n74-ne17.
Johnson, A., Bulgarelli, L., Pollard, T., Celi, LA, Mark, R., & Horng, S. (2023). MIMIC-IV-ED (versão 2.2). FisioNet. https://doi.org/10.13026/5ntk-km72.
Johnson, A., Pollard, T., Mark, R., Berkowitz, S., & Horng, S. (2019). Banco de dados MIMIC-CXR (versão 2.0.0). PhysioNet. https://doi.org/10.13026/C2JT1Q.
