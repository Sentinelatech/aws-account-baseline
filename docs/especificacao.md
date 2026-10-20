# Especificação — aws-account-baseline

**Semana:** 04/11 a 10/11/2026
**Entrega final:** relatório de baseline + evidências

## Contexto

Uma conta AWS nova acaba de ser aberta. Antes de qualquer carga rodar nela, você precisa deixá-la segura e documentar o estado contra o CIS AWS Foundations Benchmark, para que uma auditoria futura tenha por onde começar.

## Escopo

1. **Proteger a raiz** — MFA na conta root, remover chaves de acesso da root, criar um usuário administrador individual com MFA.
2. **Identidade** — política de senha, grupos em vez de permissões soltas, IAM Access Analyzer ligado.
3. **Rastro e orçamento** — alerta de orçamento (US$ 1, 5 e 10), CloudTrail em todas as regiões gravando num bucket S3 cifrado e privado.
4. **Exposição** — Block Public Access ligado no nível da conta.
5. **Medir** — para cada controle do recorte do CIS, marcar o estado antes, a ação e a evidência.

## Critério de aceite

- [ ] Alerta de orçamento criado **antes** de tudo
- [ ] Root com MFA e sem chaves; admin individual com MFA
- [ ] CloudTrail multi-região com bucket cifrado e privado
- [ ] Block Public Access e Access Analyzer ligados
- [ ] Relatório item a item contra o CIS, com evidência (print com a conta ocultada)
- [ ] README com o resultado em uma linha

## Fora de escopo

Subir serviços pagos; criar recursos que fogem do plano gratuito.

## Fases (issues da semana)

| Dia | Fase | Entrega do dia |
|---|---|---|
| Qua 04/11 | Orçamento e proteção da raiz | Alerta ativo, root com MFA |
| Qui 05/11 | Usuário admin e política de senha | Admin individual com MFA |
| Sex 06/11 | CloudTrail e bucket de logs | Trilha multi-região gravando |
| Sáb 07/11 | Block Public Access e Access Analyzer (dia leve) | Os dois ligados |
| Dom 08/11 | Recolher evidências (dia leve) | Prints organizados em `evidencias/` |
| Seg 09/11 | Comparação com o CIS | Relatório item a item em rascunho |
| Ter 10/11 | Fechamento | Relatório final e README |
