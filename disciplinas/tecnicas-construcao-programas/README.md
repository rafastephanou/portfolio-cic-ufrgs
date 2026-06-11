# 🧩 Técnicas de Construção de Programas (INF01120)

**Período:** 2025/2
**Projeto:** Bookly — gestão de clubes do livro digitais
**Professora:** Karina Kohl 

> 🔗 **Repositório do projeto:** [github.com/rafastephanou/Bookly](https://github.com/rafastephanou/Bookly)
> Lá estão a documentação técnica completa, instruções de execução e integração contínua.

---

## 🎯 O problema

**Bookly** é uma aplicação desktop em Java/Swing que digitaliza a organização de clubes do livro: criar clubes, cadastrar livros, abrir **votações** (para escolher o livro e a data-limite de leitura) e marcar **encontros** entre os participantes.

Mais do que o domínio em si, o projeto foi o veículo para praticar os conceitos da disciplina — **reuso, modularização, testes e qualidade de código**.

---

## 🏗️ Arquitetura e tecnologias

- **Java 17 + Swing** (interface gráfica)
- **Arquitetura em camadas:** `model` (entidades) · `repository` (persistência em arquivos) · `service` (regras de negócio) · `view` (telas) + controladores ligando interface e lógica
- **Persistência baseada em arquivos** (CSV)
- **Reuso de bibliotecas:** tinylog (_logging_) e JCalendar (datas)
- **Testes:** JUnit 5
- **CI:** GitHub Actions compila e roda os testes a cada _push_

---

## 👤 Minhas contribuições

Atuei principalmente na **lógica de negócio, na persistência e nos testes**:

- **Camada de serviço (regras de negócio):** implementei `BookClubService` e `UserService`, a auxiliei no desenvolvimento da classe gerenciadora central `AppSystem`.
- **Camada de persistência:** desenvolvi o `UserRepository` e a leitura/escrita dos dados em arquivos CSV.
- **Testes automatizados:** escrevi grande parte da suíte unitária (usuários, clubes, votações, encontros), garantindo cobertura das entidades de domínio.
- **Integração e ponto de entrada:** trabalhei no `Main` e na ligação entre as camadas.

---

## 🤝 Trabalho em equipe

O projeto foi desenvolvido em grupo, junto dos alunos Leonardo Leites, Matheus Candiotto e Victor Hugo Silveira. Adotamos um fluxo de **branches e Pull Requests**, com branches de uso pessoal para facilitar a **resolução de conflitos de merge** ao integrar o trabalho de cada um.

---

## 🧠 Conceitos da disciplina aplicados

- **Reuso de software** — bibliotecas externas, herança entre superclasses/subclasses e um sistema de _logging_ reutilizado de forma extensiva
- **Modularização e baixo acoplamento** —  adotamos a arquitetura em camadas, com a divisão entre classes de permanência, lógica de negócio e interface. 
- **Testes automatizados** e verificação contínua
- **Versionamento com Git** — branches, PRs e commits descritivos

---

## 📈 Resultados e aprendizados

- A separação do projeto em camadas se mostrou muito efetiva em isolar as responsabilidades e facilitar a escrita dos testes
- Passei muito tempo resolvendo conflitos de merge entre branches que poderiam ter sido evitados com pushes menores e integração mais frequente.
- Uma maior ênfase em CI certamente teria agilizado enormemente o processo de desenvolvimento.

