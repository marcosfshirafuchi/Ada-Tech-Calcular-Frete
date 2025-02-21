# CEP Checker - Validação e Consulta de CEP

## Descrição
O CEP Checker é uma API em Java projetada para aprimorar a precisão e a velocidade das consultas de CEP. Ela visa solucionar problemas comuns enfrentados por plataformas de e-commerce e outros sistemas que dependem de endereços precisos para calcular fretes e garantir um checkout eficiente, oferecendo uma experiência otimizada para o usuário.

## Problema Resolvido
- Otimização de Consultas de CEP:
  - Implementação de sistema de cache para armazenar resultados de consultas frequentes, reduzindo o tempo de resposta e latência.
  - Utilização de APIs de CEP confiáveis e de alta performance, que oferecem consultas rápidas e precisas.
  - Infraestrutura escalável para suportar o volume de consultas, evitando lentidão em horários de pico.
- Enriquecimento de Dados Geográficos:
  - Integração com o banco de dados do IBGE para obter informações detalhadas sobre a região do CEP, como bairro, cidade, estado e coordenadas geográficas.
  - Cálculo de distância entre vendedor e comprador utilizando as coordenadas geográficas, permitindo o cálculo preciso do frete.
- Validação e Correção de CEPs:
  - Validação do CEP em tempo real durante o cadastro, alertando o usuário sobre possíveis erros e oferecendo sugestões de correção.
  - Normalização de dados para corrigir automaticamente erros de formatação nos CEPs.
  - Banco de dados atualizado de CEPs, incluindo informações sobre CEPs especiais e áreas de risco.

## Demonstração
A API pode ser consultada via requisições HTTP:
```bash
GET /cep/{cep}
```
**Exemplo de Resposta:**
```json
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "bairro": "Sé",
  "cidade": "São Paulo",
  "estado": "SP",
  "latitude": -23.55052,
  "longitude": -46.633308
}
```

## Como Instalar
1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/cep-checker.git
```
2. Acesse o diretório do projeto:
```bash
cd cep-checker
```
3. Instale as dependências via Maven:
```bash
mvn clean install
```

## Como Executar
1. Inicie a aplicação:
```bash
mvn spring-boot:run
```
2. Acesse a API via browser ou ferramenta como Postman:
```bash
http://localhost:8080/cep/01001-000
```

## Como Contribuir
1. Fork o repositório.
2. Crie uma nova branch:
```bash
git checkout -b minha-feature
```
3. Faça suas alterações e commit:
```bash
git commit -m "Adicionando nova funcionalidade"
```
4. Envie para o repositório remoto:
```bash
git push origin minha-feature
```
5. Abra um Pull Request para revisão.

---

**Licença**
Este projeto está licenciado sob a [MIT License](LICENSE).

