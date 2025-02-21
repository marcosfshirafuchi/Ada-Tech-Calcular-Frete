# CEP Checker - Validação e Consulta de CEP

## Descrição
O **CEP Checker** é uma API em Java projetada para melhorar a precisão e a velocidade das consultas de CEP. Ele resolve problemas comuns enfrentados por plataformas de e-commerce e sistemas que dependem de endereços precisos para calcular fretes e garantir um checkout eficiente.

## Problema Resolvido
- Corrige erros e lentidão em consultas de CEP, proporcionando uma melhor experiência ao usuário.
- Fornece informações detalhadas sobre a região do comprador, auxiliando nos cálculos de entrega.
- Identifica e trata CEPs inexistentes ou mal formatados, evitando falhas no checkout.

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

