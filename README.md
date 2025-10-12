<h1 align="center">
  <br>
  Laboratório de Cibersegurança: Desafio DIO
</h1>

<p align="center">
  🔒 Testes de Penetração em Ambiente Controlado
</p>

---

### **🚀 Sobre o Projeto**

Este repositório documenta um laboratório de testes de penetração e análise de vulnerabilidades, criado como parte do desafio do bootcamp **Cibersegurança** da plataforma **DIO**. O objetivo principal foi aplicar conhecimentos teóricos em um ambiente prático e seguro, simulando cenários de ataques reais para fins educacionais.

A infraestrutura do laboratório foi montada com as seguintes máquinas virtuais:

* **Kali Linux**: Máquina atacante, equipada com um conjunto robusto de ferramentas de segurança.
* **Metasploitable 2**: Máquina alvo, intencionalmente vulnerável, utilizada para identificar e explorar falhas.

As VMs foram configuradas em uma **rede privada (Host-Only)** para garantir o isolamento e a segurança do ambiente.

---

### **🧪 Experimentos Realizados**

#### **1. Exploração do Serviço FTP com Metasploit**

Um ataque direcionado a uma vulnerabilidade de serviço para obter acesso remoto ao sistema.

**Passos do Ataque:**

* **Reconhecimento (Nmap)**: Um escaneamento de portas revelou o serviço `vsftpd 2.3.4` na porta **21** do alvo, uma versão com uma backdoor conhecida.
* **Exploração (Metasploit)**: O exploit `vsftpd_234_backdoor` foi utilizado para tomar controle da máquina, resultando em uma shell de comando com privilégios de acesso.

<p align="center">
  <img src="https://img.shields.io/badge/Ataque-Metasploit-blue?style=flat-square">
  <img src="https://img.shields.io/badge/Alvo-vsftpd%202.3.4-red?style=flat-square">
</p>

#### **2. Ataque de Força Bruta em Aplicação Web (DVWA)**

Demonstração prática de como senhas fracas e a falta de validação de login podem comprometer a segurança.

**Passos do Ataque:**

* **Preparação**: Utilizou-se o **Hydra** em conjunto com a wordlist `rockyou.txt` para testar milhões de senhas.
* **Execução**: O ataque foi direcionado à página de login do **DVWA**. Embora o ataque inicial tenha retornado múltiplos "falsos positivos", o problema foi solucionado ao ajustar o comando para buscar a string de sucesso `"Welcome"`, garantindo a identificação da única senha válida: **`password`**.

<p align="center">
  <img src="https://img.shields.io/badge/Ferramenta-Hydra-green?style=flat-square">
  <img src="https://img.shields.io/badge/Alvo-DVWA-yellow?style=flat-square">
</p>

---

### **📸 Evidências dos Testes**

Para uma visualização detalhada de cada etapa e dos resultados, confira as capturas de tela dos testes na pasta [`screenshots_lab`](./https://github.com/JLucFelix/Laboratorio_KALI/blob/main/screenshots_lab.zip).

---

### **📚 Conclusão**

Este projeto é um passo inicial para o domínio do pentest e um forte pilar para minha jornada na área de cibersegurança. Ele demonstra habilidades práticas em:

* **Análise de Vulnerabilidades**
* **Ataques de Força Bruta**
* **Exploração de Serviços**
* **Utilização de Ferramentas** (Nmap, Metasploit, Hydra)

O próximo passo é explorar outras vulnerabilidades do DVWA, como **Injeção de SQL** e **Cross-Site Scripting (XSS)**, para aprimorar ainda mais as habilidades técnicas.
