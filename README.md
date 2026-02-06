# Projeto Medusa – Ataques de Força Bruta

Este projeto foi desenvolvido como parte do desafio da DIO, com o objetivo de simular ataques de força bruta em ambientes controlados utilizando Kali Linux e a ferramenta Medusa.

## Ambiente
- Kali Linux
- Metasploitable 2
- DVWA
- VirtualBox (rede host-only)

## Ferramentas Utilizadas
- Medusa
- Nmap
- DVWA
- FTP / SMB

## Atividades Realizadas
- Enumeração de usuários
- Password spraying em SMB
- Ataque de força bruta em serviços
- Testes em ambiente vulnerável

## Mitigações
- Uso de senhas fortes
- Limitação de tentativas de login
- MFA
- Monitoramento de logs

## Considerações Finais
Projeto realizado para fins educacionais, em ambiente controlado.

## Execução do Ataque SMB (Password Spraying)

Neste teste foi realizado um ataque de password spraying no serviço SMB da máquina vulnerável, utilizando a ferramenta Medusa em ambiente controlado.

### Enumeração de Usuários
Foi utilizada uma lista simples de usuários previamente identificados durante a fase de enumeração.

### Comando Utilizado

```bash
medusa -h 192.168.56.104 -U smb_users.txt -P senhas_spray.txt -M smbnt -t 2 -T 50
