

### Padrao de Diretorios
??? "📂 Fiorilli"
    ??? "📁 Arquivos"
        ??? "📁 SIA7"
            - 📦 Arquivos de instalação do SIA

    ??? "📁 Auxiliares"
        ??? "📦 Softwares auxiliares ao suporte"
            - 🧠 IBExpert
            - ☕ Java
            - 🔥 Firebird
            - 📝 Notepad++

    ??? "📁 Bancos"
        ??? "📁 SIA7"
            ??? "📁 SGB_DADOS"
                - 🗄️ SIADADOS.FDB
                - 🗄️SIAARQUIVOS.FDB

    ??? "📁 Web"
        ??? "📁 JBOSS_SIA ou PM"
            ??? "📁 jboss"
                - ⚙️ Arquivos do JBoss


---

## Instalacao Firebird
??? "🛠️ Instalação Firebird 2.5.9"
    **Passos:**
    ??? "1. Realize o download do Firebird" 
        > O link para download está na seção de links úteis  
        > Siga o padrão dos diretórios e salve-o na pasta auxiliares
    

    ??? "2. Descompacte o arquivo" 
        > Após descompactar, você verá os arquivos em sua pasta 
        >
        >Escolha a arquitetura correta do servidor (32 ou 64 bits)
        >
        > Clique no executavel
        ![alt text](image.png)
        
       
    ??? "3. Siga a instalcacao"
        ![alt text](image-1.png)
        > Clique em OK
        ---
        ![alt text](image-2.png)
        > Clique em Seguinte
        ---
        ![alt text](image-3.png)  
        > Aceite os termos e clique em seguinte 
        ---
        ![alt text](image-4.png) 
        > Clique em Seguinte
        ---
        ![alt text](image-5.png)
        > Renomeie a pasta onde o firebirde sera instalado padrao adotado Firebird_versao_nomeSistema_Porta
        >
        >Exemplo: Firebird_2_5_SIA_3055
        ---
        ![alt text](image-6.png)
        > Selecione a opcao Binarios Classic Server depois clique em seguinte
        ---
        ![alt text](image-7.png)
        > Clique em seguinte
        ---
        ![alt text](image-8.png)
        > Marque as opcoes conforme a imagem
        ---
        ![alt text](image-9.png)
        > Clique em instalar
        ---
        ![alt text](image-10.png)
        > Clique em seguinte
        ---
        ![alt text](image-11.png)
        > Desmarque as opcoes e clique em concluir
    ??? "4. Volte a pasta onde o arquivo foi descompactado"
        > De acordo com a quantidade de memoria RAM selecione um arquivo de configuracao
        >
        > Neste exemplo iremos considerar um servidor de 32GB de RAM , desta forma iremos copiar o arquivo com a capacidade de recurso correspondente.
    ??? "5. Nevegue ate a pasta onde o Firebird foi instalado"
        > Neste caso navegue ate: C:\Program Files\Firebird\Firebird_2_5_SIA_3055
        >
        > Cole o arquivo no diretorio
        ![alt text](image-12.png)
        >
        > Encontre o arquivo firebir.conf e renomeeo para firebird_old.conf e renomeie o arquivo firebird_2.5.9_SuperClassic_64bits_32GB.conf para firebird.conf
        >
        >
        ![alt text](image-15.png)
    ??? "6. Definindo porta de conexao no arquivo"
        > Utilize um editor de texto e abra o arquivo renomeado para firebird.conf
        >
        >Faca uma pesquisa no arquivo no Windows utilize as teclas CTRL + F e digite RemoteServicePort
        >
        > A porta padrao do Firebird e a 3050, porem como definimos na criacao da pasta como 3055 basta alterar o campo para 3055 e salvar o arquivo
        >
        ![alt text](image-16.png)

    ??? "7. Instalando o servico"
        > Agora abra com cmd 
        >
        > Utilize o comando cd para navegar ate o diretorio de instalacao do Firebird e acesse a pasta bin
        >
        > No nosso caso: C:\Program Files\Firebird\Firebird_2_5_SIA_3055\bin
        >
        ![alt text](image-17.png)
        >
        > Digite o seginte comando instsvc i -m -a -n Firebird_2_5_SIA_3055
        >
        > instsvc i -m -a -n é o comando para criar a instancia do serviço do Firebird. 
        >
        > Firebird_2_5_SIA_3055 é o nome da instancia do serviço do Firebird.
        >
        > Note que o nome do service e o mesmo nome que demos a pasta de instalacao do Firebird
        >
        > Agora temos o servico instalado 
        ![alt text](image-18.png)
---

## Instalacao do SIA
??? "🛠️ Instalacao do SIA7.5"
    **Passos:**
    ??? "1. Acessando o diretorio"
        > Navegue ate o diretorio padrao da instalacao 
        >
        > Fiorilli/Arquivos/SIA7