# Enem Analytics

## Descrição

O Exame Nacional do Ensino Médio (ENEM) é sem dúvidas um dos vestibulares mais importantes do país, por ser uma das principais formas de ingresso em universidades públicas, e alternativa para muitas privadas. Entretanto, vivemos em um dos países mais desiguais do mundo, e a desigualdade social e econômica pode ser um fator determinante para o desempenho dos candidatos. Esse estudo tem o intuito de investigar esses impactos sócio-demográficos, e entender como eles influenciam a nota dos candidatos.

## Fonte dos Dados

Os dados principais utilizados nesse notebook foram extraídos do site do INEP, na seção de microdados do ENEM 2023: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem

Ao baixar os microdados, utilizamos apenas a base MICRODADOS_ENEM_2023, que contém informações sobre os candidatos, suas notas, e suas condições sócio-demográficas. A base as seguintes colunas:

- NU_INSCRICAO: Número de inscrição

- NU_ANO: Ano do Enem
- TP_FAIXA_ETARIA: Faixa etária
- TP_SEXO: Sexo
- TP_ESTADO_CIVIL: Estado Civil
- TP_COR_RACA: Cor/raça
- TP_NACIONALIDADE: Nacionalidade
- TP_ST_CONCLUSAO: Situação de conclusão do Ensino Médio
- TP_ANO_CONCLUIU: Ano de Conclusão do Ensino Médio
- TP_ESCOLA: Tipo de escola do Ensino Médio
- TP_ENSINO: Tipo de instituição que concluiu ou concluirá o Ensino Médio
- IN_TREINEIRO: Indica se o inscrito fez a prova com intuito de apenas treinar seus conhecimentos
- CO_MUNICIPIO_ESC: Código do município da escola
- NO_MUNICIPIO_ESC: Nome do município da escola
- CO_UF_ESC: Código da Unidade da Federação da escola
- SG_UF_ESC: Sigla da Unidade da Federação da escola
- TP_DEPENDENCIA_ADM_ESC: Dependência administrativa (Escola)
- TP_LOCALIZACAO_ESC: Localização (Escola)
- TP_SIT_FUNC_ESC: Situação de funcionamento (Escola)
- CO_MUNICIPIO_PROVA: Código do município da aplicação da prova
- NO_MUNICIPIO_PROVA: Nome do município da aplicação da prova
- CO_UF_PROVA: Código da Unidade da Federação da aplicação da prova
- SG_UF_PROVA: Sigla da Unidade da Federação da aplicação da prova
- TP_PRESENCA_CN: Presença na prova objetiva de Ciências da Natureza
- TP_PRESENCA_CH: Presença na prova objetiva de Ciências Humanas
- TP_PRESENCA_LC: Presença na prova objetiva de Linguagens e Códigos
- TP_PRESENCA_MT: Presença na prova objetiva de Matemática
- CO_PROVA_CN: Código do tipo de prova de Ciências da Natureza
- CO_PROVA_CH: Código do tipo de prova de Ciências Humanas
- CO_PROVA_LC: Código do tipo de prova de Linguagens e Códigos
- CO_PROVA_MT: Código do tipo de prova de Matemática
- NU_NOTA_CN: Nota da prova de Ciências da Natureza
- NU_NOTA_CH: Nota da prova de Ciências Humanas
- NU_NOTA_LC: Nota da prova de Linguagens e Códigos
- NU_NOTA_MT: Nota da prova de Matemática
- TX_RESPOSTAS_CN: Vetor com as respostas da parte objetiva da prova de Ciências da Natureza
- TX_RESPOSTAS_CH: Vetor com as respostas da parte objetiva da prova de Ciências Humanas
- TX_RESPOSTAS_LC: Vetor com as respostas da parte objetiva da prova de Linguagens e Códigos
- TX_RESPOSTAS_MT: Vetor com as respostas da parte objetiva da prova de Matemática
- TP_LINGUA: Língua Estrangeira
- TP_STATUS_REDACAO: Situação da redação do participante
- NU_NOTA_COMP1: Nota da competência 1 da redação
- NU_NOTA_COMP2: Nota da competência 2 da redação
- NU_NOTA_COMP3: Nota da competência 3 da redação
- NU_NOTA_COMP4: Nota da competência 4 da redação
- NU_NOTA_COMP5: Nota da competência 5 da redação
- NU_NOTA_REDACAO: Nota da prova de redação
- Q001: Até que série seu pai, ou o homem responsável por você, estudou?
- Q002: Até que série sua mãe, ou a mulher responsável por você, estudou?
- Q003: A partir da apresentação de algumas ocupações divididas em grupos ordenados, indique o grupo que contempla a ocupação mais próxima da ocupação do seu pai ou do homem responsável por você. (Se ele não estiver trabalhando, escolha uma ocupação pensando no último trabalho dele).
- Q004: A partir da apresentação de algumas ocupações divididas em grupos ordenados, indique o grupo que contempla a ocupação mais próxima da ocupação da sua mãe ou da mulher responsável por você. (Se ela não estiver trabalhando, escolha uma ocupação pensando no último trabalho dela).
- Q005: Incluindo você, quantas pessoas moram atualmente em sua residência?
- Q006: Qual é a renda mensal de sua família? (Some a sua renda com a dos seus familiares.)
- Q007: Em sua residência trabalha empregado(a) doméstico(a)?
- Q008: Na sua residência tem banheiro?
- Q009: Na sua residência tem quartos para dormir?
- Q010: Na sua residência tem carro?
- Q011: Na sua residência tem motocicleta?
- Q012: Na sua residência tem geladeira?
- Q013: Na sua residência tem freezer (independente ou segunda porta da geladeira)?
- Q014: Na sua residência tem máquina de lavar roupa? (o tanquinho NÃO deve ser considerado)
- Q015: Na sua residência tem máquina de secar roupa (independente ou em conjunto com a máquina de lavar roupa)?
- Q016: Na sua residência tem forno micro-ondas?
- Q017: Na sua residência tem máquina de lavar louça?
- Q018: Na sua residência tem aspirador de pó?
- Q019: Na sua residência tem televisão em cores?
- Q020: Na sua residência tem aparelho de DVD?
- Q021: Na sua residência tem TV por assinatura?
- Q022: Na sua residência tem telefone celular?
- Q023: Na sua residência tem telefone fixo?
- Q024: Na sua residência tem computador?
- Q025: Na sua residência tem acesso à Internet?

Além da base de microdados do ENEM, será utilizada uma base complementar com informações sobre o IDH dos municípios brasileiros, que foi extraída do site do Atlas Brasil: http://www.atlasbrasil.org.br/consulta/planilha

## Integrantes
- Ubiratan da Motta Filho R.A 20.00928-3
- Joao Paulo M Socio 20.00704-3
- Luan Teixeira R.A: 20.01681-6
- Bruno Davidovitch Bertanha 20.01521-6