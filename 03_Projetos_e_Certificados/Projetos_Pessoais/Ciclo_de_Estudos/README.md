# Ciclo de Estudos

## Problema
Distribuir sessões de estudo ao longo da semana e conhecer a carga horária planejada.

## Solução e funcionalidades
Adicionar disciplina, dia e duração; remover sessões; somar minutos e horas; salvar automaticamente neste navegador; exportar o planejamento em JSON e limpar os dados com confirmação.

## Tecnologias e execução
HTML, CSS e JavaScript, sem servidor. Abra `docs/ciclo/index.html`, na raiz do repositório. Dados em `localStorage`, sob a chave `study-hub-ciclo-v1`.

## Critérios de aceite
- Nome vazio não é aceito.
- Duração deve ser inteira entre 10 e 240 minutos.
- Sessão adicionada aparece na lista e no total.
- Remover atualiza a lista e a soma.
- Recarregar mantém os dados quando o armazenamento está disponível.
- Exportação gera JSON com as sessões.

## Limitações
Não há sincronização entre aparelhos. Limpar dados do navegador apaga o planejamento. Falha no armazenamento exibe aviso; a lista continua disponível apenas durante a sessão. O projeto é uma ferramenta de organização, sem prescrição de carga de estudos.

Autor: Luís Flávio Góis da Silva.
