# Projeto de Testes de Força Bruta com Kali Linux e Medusa 

Este projeto foi feito como parte de um desafio no Bootcamp de Cibersegurança da DIO para compreender sobre **ataques de força bruta** e o uso do **Kali Linux** junto com a ferramenta **Medusa**.  
É o meu primeiro contato com essas ferramentas e com a ideia de simular ataques de força bruta, então o foco foi mais em entender o funcionamento básico do ambiente e como os testes são feitos.

---

## Objetivo

Simular ataques de **força bruta** em diferentes serviços e entender como esses ataques acontecem na prática, além de pensar em formas de **prevenir** esse tipo de vulnerabilidade.

---

## Configuração do Ambiente

O ambiente foi criado no **VirtualBox** com **duas máquinas virtuais**:
- **Kali Linux** (máquina atacante)
- **Metasploitable 2** (máquina vulnerável)

As duas estão configuradas em rede **interna (host-only)** para que consigam se comunicar sem acesso à internet.

---

## Testes Realizados

Durante o projeto, tentei realizar três tipos de simulações:

1. **Ataque de força bruta em FTP** usando o Medusa  
   → Aqui usei uma wordlist simples e consegui entender como a ferramenta tenta várias senhas automaticamente.

2. **Ataque em formulário web (DVWA)**  
   → Testei o envio automático de logins com senhas diferentes até conseguir o acesso.

3. **Password spraying em SMB**  
   → Testei uma forma diferente de ataque, onde a mesma senha é testada para vários usuários. Também foi possível ver como a enumeração de usuários funciona.

---

## Documentação dos Testes

- Wordlists usadas: listas pequenas de exemplo, criadas manualmente.  
- Comando principal utilizado (exemplo):
  ```bash
   medusa -h 192.168.56.101 -U users.txt -P pass.txt -M ftp -t 6
  

## Observação

Este projeto é apenas educacional, feito em ambiente controlado e isolado.
