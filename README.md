# Playbook de Configuração do Filebeat para captura de logs do swarm
Esse playbook foi criado para automatizar a configuração da captura de logs dos microserviços e envio para o elasticsearch
O pĺaybook realiza as seguintes etapas em todos os nós do swarm
* Cria um arquivo de serviço filebeat para o novo microserviço
* Cria um arquivo de configuração do filebeat para captura dos logs do microserviço
* Inicializa o serviço do filebeat para o microserviço criado

## Configuração
Para rodar o playbook voce precisa editar as seguintes variáveis
* nome_microservico = nome do microserviço que ira gerar os logs
* imagem = nome da imagem utilizada pelo microservico
* hostname = hostname do elasticsearch que ira receber os dados

### Execução
Para executar o playbook basta executar o comando
```
ansible-playbook filebeat.yaml -k
```

O comando acima irá solicitar pelo password do usuário root para que o pĺaybook seja executado
