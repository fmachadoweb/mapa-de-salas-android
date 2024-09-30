# Sistema de Mapa de Salas de Aula

## Visão Geral
O **Sistema de Mapa de Salas de Aula** é um aplicativo Android desenvolvido em **Kotlin**, utilizando **WebView** para exibir informações sobre a disponibilidade e ocupação das salas de aula de uma instituição de ensino. O aplicativo oferece uma interface intuitiva para a visualização e atualização dessas informações, com acesso restrito para colaboradores autorizados.

## Tecnologias Utilizadas
- **Android (Kotlin com WebView)**
- **PHP** (backend)
- **SQL** (banco de dados)
- **HTML, CSS, JavaScript** (interface web)
- **AJAX** (comunicação assíncrona)

## Funcionalidades Principais

### Visualização do Mapa de Salas
- Exibição interativa do mapa de salas de aula.
- Grade semanal (segunda a sexta) mostrando a disponibilidade das salas.
- Indicação de status de ocupação (disponível/ocupada).
- Informações sobre o uso da sala (professor, setor responsável).

### Área Restrita para Colaboradores
- Autenticação segura por login.
- Permite a atualização do status de ocupação das salas.
- Interface para modificar status, responsável pela sala e horários.

### Sistema de Log
- Registra tentativas de login.
- Armazena detalhes das modificações realizadas no sistema.
- Facilita o controle e rastreamento das atualizações.

## Arquitetura do Sistema

### Frontend (Aplicativo Android)
- Desenvolvido em **Kotlin** para Android.
- Utiliza **WebView** para renderizar a interface web responsiva (HTML, CSS e JavaScript).
- Faz uso de **AJAX** para comunicação assíncrona com o backend.

### Backend (Servidor)
- Servidor em **PHP** para processamento das requisições.
- Banco de dados **SQL** para armazenar as informações de salas e usuários.
- API **RESTful** para comunicação entre o aplicativo e o servidor.

## Fluxo de Dados
1. O aplicativo Android carrega a interface web através do **WebView**.
2. A interface faz requisições **AJAX** ao servidor **PHP** para obter dados sobre a ocupação das salas.
3. O servidor consulta o banco de dados **SQL** e retorna as informações.
4. A interface web é atualizada dinamicamente com os dados recebidos.
5. Para atualizações de dados (ex.: modificar ocupação), o aplicativo envia requisições **POST** para o servidor, que processa e grava as informações no banco de dados.

## Segurança
- Autenticação por login para acessar a área restrita.
- Senhas armazenadas de forma criptografada no banco de dados.
- Proteção contra **injeções SQL** e **XSS** por meio de validação de entrada.
- Utilização de **HTTPS** para garantir segurança na comunicação entre o aplicativo e o servidor.

## Manutenção e Atualizações
- Realizar backups periódicos do banco de dados.
- Aplicar atualizações de segurança nas tecnologias utilizadas.
- Revisar e otimizar o código regularmente para correção de bugs e melhorias de desempenho.

## Considerações Futuras
- Implementação de **notificações push** para alertar sobre alterações de status das salas em tempo real.
- Expansão para incluir funcionalidades de **reserva de salas**.
- Desenvolvimento de uma versão web completa para acesso por navegadores.

## Como Contribuir
Para contribuir com o projeto, siga os seguintes passos:
1. Faça um fork do repositório.
2. Crie um branch com a sua feature (`git checkout -b feature/MinhaFeature`).
3. Faça commit das suas alterações (`git commit -m 'Adiciona MinhaFeature'`).
4. Envie para o branch (`git push origin feature/MinhaFeature`).
5. Abra um Pull Request.

## Licença
Este projeto está licenciado sob os termos da licença MIT.
