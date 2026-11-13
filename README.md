# Comando — comando da TV no telemóvel

> **Atualização:** esta TV ignora a API de comando da Samsung. Por isso, o comando já não fala diretamente com a TV.
> As ordens passam pelo servidor MQTT público e gratuito da HiveMQ (`broker.hivemq.com`), num canal com o código secreto que aparece no canto do Home.
> É o próprio Home, a correr na TV, que as executa. Para ligar, escreve esse código no telemóvel.
> As setas só mexem dentro do Home. Não há botão para ligar nem desligar a TV.
> Algumas das instruções abaixo (IP da TV, aviso de segurança, pedido de autorização na TV) são da versão antiga e já não se aplicam.

É uma página web (`index.html`).

## O que faz
- **Ligar/desligar** a TV, mudar de **fonte** e abrir as **definições**.
- Usar as **setas**, o **OK**, o **Voltar** e o **Sair**.
- Mudar o **volume**, tirar o som, mudar de **canal** e abrir a **lista de canais**. Se mantiveres o dedo nas setas, no volume ou nos canais, a ação repete-se.
- Escrever o número de um canal no **teclado numérico** (botão 123).
- Usar os botões de **multimédia**: recuar, play, pausa e avançar.
- **Abrir apps** na TV. O botão “Ver todas as apps da TV” vai buscar a lista verdadeira das apps instaladas, já com os IDs certos.
- **Início**: abre o nosso home screen.

## Pôr na internet (GitHub Pages, grátis)
1. Cria uma conta em https://github.com/signup.
2. Carrega em **+ → New repository**. Dá-lhe o nome `comando`, escolhe **Public** e carrega em **Create repository**.
3. Na página do repositório, carrega em **uploading an existing file** e arrasta o `index.html` desta pasta. Depois carrega em **Commit changes**.
4. Vai a **Settings → Pages**. Em *Branch*, escolhe **main** e **/(root)** e carrega em **Save**.
5. Ao fim de 1 ou 2 minutos, o comando fica disponível em:
   `https://O-TEU-UTILIZADOR.github.io/comando/`

Abre esse link no telemóvel e adiciona-o ao ecrã principal.
Para atualizar o comando no futuro, basta carregar outra vez um `index.html` novo no repositório.

## Usar
1. O telemóvel e a TV têm de estar na **mesma rede Wi-Fi**.
2. Abre a página no telemóvel e escreve o **IP da TV** (Definições → Geral → Rede → Estado da rede → Definições IP).
3. Na primeira vez, a TV pergunta se aceitas o “Comando Home”. Carrega em **Permitir**.
4. Se não ligar, abre no telemóvel o link que a página mostra (`https://IP-DA-TV:8002/api/v2/`). Aceita o aviso de segurança (“Avançadas” → “Continuar”) e volta a tentar.
5. Se o browser perguntar se a página pode **aceder a dispositivos na rede local**, carrega em **Permitir**. Sem isso, não consegue falar com a TV.
6. Para parecer uma app, no menu do browser escolhe **Adicionar ao ecrã principal**.

## Limites
- **Ligar a TV:** só funciona se a TV ainda estiver “acordada” na rede. Para que fique, liga em Definições → Geral → Rede → Definições Avançadas → **Ligar com telemóvel** (*Power On with Mobile*). Se a TV estiver desligada há muito tempo, pode ser preciso o comando normal.
- A página tem de estar alojada num sítio a que o telemóvel consiga chegar (vê as opções no chat).
