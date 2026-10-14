# aws-account-baseline

Endurecimento de uma conta AWS a partir do zero e relatório comparando o estado da conta com o **CIS AWS Foundations Benchmark**. É o trabalho de governança e identidade que toda empresa precisa fazer ao abrir uma conta de nuvem.

> Projeto 3 de 7 do laboratório [sentinelatech](https://github.com/sentinelatech). Área: **governança e IAM**.

## Por que isso importa em segurança

A maioria dos incidentes em nuvem começa em configuração errada: conta root sem proteção, credencial exposta, bucket aberto. Saber estabelecer uma baseline e medir a conta contra um padrão reconhecido é o básico de cloud security e aparece em auditoria, GRC e IAM.

## Objetivo

Deixar a conta AWS em um estado seguro mínimo e entregar um relatório que, item a item, compare a conta com os controles do CIS Benchmark, com evidência de cada ajuste.

## Estrutura

```
docs/especificacao.md   escopo e critério de aceite
docs/controles.md       os controles aplicados, explicados
relatorio/              o relatório de baseline (antes / depois / evidência)
evidencias/             prints com o ID da conta ocultado
```

## Controles cobertos

Conta root com MFA e sem chaves de acesso · usuário administrador individual com MFA · política de senha · alerta de orçamento · CloudTrail em todas as regiões, com log em bucket cifrado · Block Public Access na conta · IAM Access Analyzer ligado.

## Custo

Tudo cabe no plano gratuito. O CloudTrail com uma trilha de eventos de gerenciamento é gratuito; o bucket de logs gera centavos. Configure o alerta de orçamento **antes** de qualquer outra coisa.

## Resultado

<!-- Preencher ao fim -->

## Aviso

Nenhuma credencial, chave ou ID de conta é versionado. Os prints têm o número da conta ocultado.
