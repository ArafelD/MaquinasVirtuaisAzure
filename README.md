# 🚀 Criando uma Máquina Virtual com Windows Server no Azure

> ✅ Aplica-se a: **VMs do Windows**

Como desenvolvedor sênior, gosto de manter um fluxo de criação padronizado, repetível e fácil de documentar. Aqui está um passo a passo de como **criar uma VM Windows Server 2022** no **Portal do Azure**, perfeita para testes, laboratórios ou aprendizado. 💡

---

## 🧭 Pré-requisitos

Antes de começar:

- 🔐 Você precisa de uma **conta Microsoft** com uma assinatura do Azure ativa.
- 🧪 Este guia é voltado para **fins educacionais** e não é indicado para ambientes de produção.

Se ainda não tem uma conta, crie uma gratuita aqui: [https://azure.microsoft.com/free](https://azure.microsoft.com/free)

---

## 🔐 Etapa 1: Entrar no Portal do Azure

1. Acesse o [Portal do Azure](https://portal.azure.com)
2. Faça login com sua conta Microsoft.

---

## 🖥️ Etapa 2: Criar uma Máquina Virtual

1. No topo da barra de pesquisa, digite `Máquinas virtuais` e clique na opção em **Serviços**.
2. Clique em **Criar > Máquina virtual do Azure**.
3. Na tela “Criar uma máquina virtual”, configure os seguintes campos:

### 🧱 Detalhes da Instância:

| Campo                  | Valor recomendado                                |
|------------------------|--------------------------------------------------|
| Nome da VM             | `myVM`                                           |
| Imagem                 | `Windows Server 2022 Datacenter: Azure Edition` |
| Geração                | `x64 Gen2`                                       |
| Região                 | (Selecione a mais próxima ou de sua preferência) |
| Tipo de Redundância   | `Zona única` (ou padrão)                         |

### 👤 Conta de Administrador:

- Usuário: `azureuser`
- Senha: Uma senha forte com pelo menos **12 caracteres** e complexidade.

### 🌐 Regras de Porta de Entrada:

- Permitir portas selecionadas:
  - `RDP (3389)` ✅
  - `HTTP (80)` ✅

4. Clique em **Examinar + Criar**.
5. Após a validação, clique em **Criar**.

---

## 🔗 Etapa 3: Conectar-se à Máquina Virtual

Depois que a implantação terminar:

1. Clique em **Ir para o recurso**.
2. No painel lateral da VM, clique em **Conectar > RDP**.
3. Baixe o arquivo `.rdp` e abra no seu computador.
4. Faça login com o usuário e senha definidos anteriormente.

---

## 🌐 Etapa 4: Instalar o Servidor Web (IIS)

1. Após entrar na VM, abra o **PowerShell** como Administrador.
2. Execute o seguinte comando:

```powershell
Install-WindowsFeature -name Web-Server -IncludeManagementTools

# Aguarde a instalação e, em seguida, acesse o endereço público da VM no seu navegador:

[1. Após entrar na VM, abra o **PowerShell** como Administrador.
2. Execute o seguinte comando:](http://<IP-da-VM>)

✅ Conclusão

Com isso, criamos e conectamos uma VM Windows no Azure e instalamos um servidor web básico (IIS).
Esse processo é fundamental para quem está iniciando no gerenciamento de infraestrutura em nuvem.


