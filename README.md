# DataHunter

Projeto de portfólio em estágio inicial para estudar coleta, processamento e disponibilização de dados com Python.

**Status:** estrutura inicial de configuração e conexão com banco. O pipeline de scraping, a API e o dashboard ainda não estão implementados neste repositório.

## Objetivo

Construir, de forma incremental, um fluxo que colete dados de fontes públicas, trate as informações, armazene os resultados e os disponibilize por API e interface de consulta.

## Estado atual

| Componente | Situação |
| --- | --- |
| Leitura de configuração via ambiente | Implementada em `app/core/config.py` |
| Configuração de engine, sessões e base SQLAlchemy | Implementada em `app/database/connection.py` |
| Modelos de dados | Arquivo reservado, ainda vazio |
| Coleta e transformação de dados | Planejadas |
| API REST | Planejada |
| Dashboard | Planejado |
| Agendamento, monitoramento e testes | Planejados |

## Tecnologias

**Presentes no código:** Python, SQLAlchemy e python-dotenv.

**Planejadas para evolução:** BeautifulSoup, Pandas, PostgreSQL, FastAPI, React e Docker. A presença nesta lista indica intenção de uso, não implementação concluída.

## Estrutura atual

- `app/core/config.py`: carrega variáveis de ambiente e lê `DATABASE_URL`.
- `app/database/connection.py`: configura engine, fábrica de sessões e base declarativa.
- `app/database/models.py`: reservado para os modelos de dados.

## Como acompanhar

```bash
git clone https://github.com/MaysonLima/DataHunter.git
cd DataHunter
```

Ainda não há aplicação executável de ponta a ponta, manifesto de dependências ou comandos de inicialização da API. As instruções de instalação serão adicionadas junto com uma primeira versão executável.

## Próximas etapas

- [ ] Definir dependências e documentar a configuração do ambiente.
- [ ] Implementar modelos e armazenamento.
- [ ] Criar um primeiro coletor e o tratamento dos dados.
- [ ] Disponibilizar os dados por API.
- [ ] Construir uma interface de consulta.
- [ ] Adicionar testes, logs e automação.

## Autor

[Mayson Lima dos Santos](https://maysonlima.github.io/Portfolio-Mayson-Lima-dos-Santos/)

## Licença

[MIT](LICENSE).
