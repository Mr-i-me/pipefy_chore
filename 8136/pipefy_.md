## Summary

- [Getting Started](#Document Upload)

## create a contratc
[comment]:<todo> ( todo ref! form fields xls)

## edição contrato
> *obs ao editar um contrato via `T.C` ou `Porttal` devemos 
> atualizar o pipefy, ou avisar o atendente que o card esta desatualizado  
> 
> ex: mostrar botão `atualizar` caso o pipefy esteja desatualizado


devemos pensar

## Document Upload

TODO: [image] add mind map of flw image
> [API. Ref.](https://api-docs.pipefy.com/reference/mutations/createPresignedUrl/)  
> Create a pre-signed URL and get the output url to send a PUT request with the attachment, using Postman.

```graphql
mutation {
    createPresignedUrl(input: {fileName: "teste.pdf", organizationId: <orgid>},) {
        clientMutationId
        downloadUrl
        url
    }
}
```

[Ref.]( https://api-docs.pipefy.com/reference/mutations/updateFieldsValues/)
> Update the attachment field of the card. In this case we need to get the part of downloadedurl starting from "upload/…".

```graphql
mutation {
    updateFieldsValues(input: {nodeId: <cardid>, values: {fieldId: "<field_attachment>", value:["uploads/63c330ba-9747-456d-8862-f616436ea1e8/teste.pdf"], operation: ADD}}) {
        clientMutationId
    }
}
```

da torre pro pipefy

pensar em dados alterados na torre ou no porttal pegar pessoas do contrato gravar

- data ultima atualização do pipefy
- id pipefy (retorno do create)

data_ultima_atualização_pipefy - updatedAt do pipefy

mostrar botão `atualizar` caso o pipefy esteja desatualizado

nao atacado dados sobrescritos

