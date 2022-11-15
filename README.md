# Recuperação de senha

**RF**
- O usuario deve poder recuperar sua senha informando seu e-mail;
- O usuário deve receber um e-mail com instruções de recuperação de senha;
- O usuario deve poder resetar sua senha;
**RNF**
- Utilizar Mailtrap para testar envios em ambientes de desenvolvimentos;
- Utilizar o Amazon SES para envios em produção;
- O envio de e-mail deve acontecer em segundo plano (background job);
**RN**
- O link enviado por e-mail para resetar senha deve expirar em 2h;
- O usuário precisa confirmar a nova senha ao resetar sua senha;

# Atualização do perfil
**RF**
- O Usuário deve poder atualizar seu nome, email e senha;
**RN**
- O usuário não pode alterar seu e-mail para um email já utilizado;
- Para atualizar sua senha o usuário deve informar a senha antiga;
- Para atualizar a senenha o usuário deve informar a nova senha.

# Painel do Prestador
*RF*
- O usuário deve poder listar seus agendamentos de um dia especifico.
- O prestador deve receber uma notificação sempre que houver um agendamento.
- O prestador deve poder visualizar  as notificações nao lidas.
*RNF*
- O agendamento do prestador no dia deverá ser armazenado em cache.
- As notificaçoes do prestador deve ser armazenadas no MongoDB.
- As notificações do prestador devem ser enviadas via Socket.io;
*RN*
- A notificação deve ter um status de lida ou não lida para que o prestador possa controlar.
# Agendamento dos serviços

*RF*
- O usuário deve poder listar todos os prestadores de serviços
- O usuário deve poder listar os dias de um mes com pelo menos um horario disponivel de um prestador.
- O usuário deve poder listar horarios disponiveis em um dia especifico de um prestador.
- O usuário deve poder realizar um novo agendamento com o prestador.
*RNF*
- A listagem de prestador deverá ser amazenada em cache.
*RN*
- Cada agendamento deve durar 1h exatamente.
- Os agendamentos devem estar disponiveis entre 8h as 18h (Primeiro as 8h, ultimo as 17h)
- O usuário nao pode agendar em um horario ja ocupado.
- O usuário nao pode realizar um agendamento retroativo.
