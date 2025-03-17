# Bem-vindo ao Repositório do Projecto Aceita Bitcoin

## Adicionar um Meetup
### Altere o ficheiro JSON meetups.json
- Crie uma nova entrada no objecto array "meetups" ou atualize uma de um meetup já existente seguindo o formato;
    ```javascript
        {
            "name": "Nome do Encontro",
            "location": {
                "place": "Nome do Local onde vai decorrer",
                "address": "Rua do Local",
                "city": "Cidade"
            },
            "time": "aaaa-mm-ddThh:mm:ssZ",
            "img": "https://raw.githubusercontent.com/talvasconcelos/aceita/main/public/images/meetups/'nomeDaImagemAqui.jpeg'",
            "description": "Descrição do Meetup (Se há suporte a pagamentos em LN, possível speaker...)",
            "link": "link para o registo no evento ou para o grupo de telegram mais próximo"
        }
    ```
- Agora dê upload de uma imagem do meetup para a localização *public/images/meetups*;
- Dê commit das alterações e abra um Pull Request no Repositório


## Adicionar um Patron
### Altere o ficheiro JSON patrons.json
- Crie uma nova entrada no objecto array "patrons" ou atualize uma de um patron já existente seguindo o formato;
    ```javascript
        {
            "patronName": "Nome do Patrono",
            "patronService": "Nome do Serviço do Patrono",
            "contact": "contacto(email ou numero de telefone)",
            "website": "link para o website",
            "img": "https://raw.githubusercontent.com/talvasconcelos/aceita/main/public/images/patrons/'nomeDaImagemAqui.jpeg'",
            "serviceDescription": "Descrição do Serviço"
        }
    ```
- Agora dê upload de uma imagem do patron para a localização *public/images/patrons*;
- Dê commit das alterações e abra um Pull Request no Repositório



