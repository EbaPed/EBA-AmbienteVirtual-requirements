# **Passo a Passo: Configuração de Ambiente Virtual e requirements.txt**


## **1. Criar um Ambiente Virtual**

Um ambiente virtual é uma ferramenta que ajuda a manter as dependências do projeto isoladas do sistema global, garantindo que as versões de pacotes não conflitem entre projetos.

### **1.1 Instalar o virtualenv (se necessário)**
Se o virtualenv não estiver instalado, você pode instalá-lo com o seguinte comando:

```bash
pip install virtualenv
```

### **1.2 Criar o Ambiente Virtual**

No diretório do seu projeto, execute o seguinte comando para criar um novo ambiente virtual chamado `venv`:

```bash
python -m venv venv
```

Isso criará um diretório chamado `venv` no seu projeto, que conterá o ambiente isolado.

### **1.3 Ativar o Ambiente Virtual**

- **No Windows:** Para ativar o ambiente virtual no Windows, execute o comando abaixo no terminal (no diretório do seu projeto):

```bash
.\venv\Scripts\activate
```

- **No macOS/Linux:** No macOS ou Linux, execute:

```bash
source venv/bin/activate
```

- **No Gitbash:** Na linha de comando do GItBash, execute:

```bash
source venv/Scripts/activate
```

Após ativar, você verá que o nome do ambiente virtual aparece no prompt (por exemplo, (venv)).

## **2. Gerar o Arquivo requirements.txt**

O arquivo requirements.txt lista todas as dependências do seu projeto, e pode ser usado para instalar esses pacotes em outros ambientes.

**2.1 Instalar Dependências Necessárias**

Com o ambiente virtual ativado, você pode instalar os pacotes que o seu projeto precisa. Por exemplo, se você precisar do pandas e seaborn:

Dentro no notebook Python, com o kernel configurado para o ambiente virtual, execute em uma célula:

```ipynb
%pip install pandas
```

Faça isto para todas bibliotecas que quer instalar.


### **2.2. Gerar o Arquivo requirements.txt**

Para gerar o arquivo requirements.txt com todas as dependências do seu ambiente virtual, execute:

```ipynb
%pip freeze > requirements.txt
```

Isso criará um arquivo requirements.txt no diretório do projeto com todas as bibliotecas instaladas no ambiente virtual.


## **3. Usar requirements.txt em um Projeto Já Existente**

Se você já tem um projeto existente e um arquivo requirements.txt, você pode configurar um ambiente virtual e instalar todas as dependências que o projeto necessita.

### **3.1 Criar e Ativar o Ambiente Virtual (se ainda não o fez)**

Siga os mesmos passos mencionados no Passo 1 para criar e ativar o ambiente virtual.

### **3.2 Instalar as Dependências Usando requirements.txt**

Depois de ativar o ambiente virtual, basta executar o seguinte comando para instalar todas as dependências que estão listadas no arquivo requirements.txt:


```ipynb
%pip install -r requirements.txt
```

Isso irá ler o arquivo requirements.txt e instalar todas as bibliotecas e suas versões especificadas.
