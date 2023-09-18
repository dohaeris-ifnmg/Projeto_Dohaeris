# Projeto Dohaeris

Projeto que visa descaracterizar aparelhos de TV Box.

## Isenção de responsabilidade (Leia com atenção)

Todo o conteúdo que você encontra neste tutorial (binários, textos, trechos de código, etc...) **não faz parte do projeto oficial da Armbian.** Dito isso, **as pessoas do projeto Armbian e nós que disponibilizamos essas documentação não somos responsáveis pelo uso indevido ou perda de funcionamento do hardware.**

## Introdução

Nesta documentação, você vai encontrar o passo a passo utilizado na instalação do sistema Armbian, sistema baseado no Debian, nos dispositivos de TV Box MXQ PRO 4K, que tem como processadores os chips Rockchip da série RK3228 A/B e RK3229.

### Especificações do modelo:

* 1GB Ram
* 7GB Armazenamento interno

### Requisitos:

* Dispositivo **TV Box MXQ PRO 4K**
* O dispositivo deve conter memórias **DDR2** e **DDR3**.
* Cartão microSD.
* Adaptador microSD para SD.
* Adaptador microSD ou SD para USB.
* Mouse e teclado USB.
* Monitor ou televisão.
* O Dispositivo TV Box deve Possuir memória **NAND**.

## Processo de instalação

- Faça o download do Multitool, uma ferramenta que permite instalar a ISO do Armbian. Além disso, o Multitool é capaz de identificar automaticamente o tipo de memória, seja NAND ou eMMC.
- Faça o download da ferramenta BalenaEtcher. Essa ferramenta será utilizada para gravar a ISO do Multitool no cartão microSD.
- Descompacte o Multitool em seu computador.
- Insira o cartão microSD no seu computador usando um adaptador SD para USB.
- Abra o BalenaEtcher.
- Selecione a opção "Flash from file" ou "Selecionar imagem" no BalenaEtcher e escolha a ISO do Multitool.
- Selecione o cartão microSD como o dispositivo de destino para a gravação.
- Clique em "Flash" ou "Gravar" para iniciar o processo de gravação no cartão microSD.
- Aguarde até que o BalenaEtcher conclua o processo de gravação no cartão microSD.
- Após a conclusão do flash, escolha uma ISO do Armbian com o kernel 4.4, de acordo com sua preferência.
- Faça o download da ISO do Armbian com o kernel 4.4 para o seu computador.
- Certifique-se de seguir as instruções adequadas para baixar a ISO do Armbian com o kernel 4.4, levando em consideração as fontes confiáveis e as etapas específicas do processo.
- Aguarde até que o download da ISO do Armbian compactado seja concluído.
- Abra o explorador de arquivos no seu computador.
- Navegue até a pasta do cartão microSD.
- Dentro da pasta, procure pela pasta "imagens".
- Mova o arquivo da ISO do Armbian compactado para essa pasta.
- Seguindo as etapas descritas anteriormente, você terá como resultado final um cartão microSD bootável com a imagem do sistema operacional Armbian.
- Coloque o cartão microSD no adaptador.
- Insira o adaptador com o cartão microSD na entrada correspondente da sua TV BOX.
- Conecte o cabo de alimentação à TV BOX.
- Aguarde alguns segundos até que o LED azul comece a piscar.
- Verifique o monitor ou televisor conectado e você verá o Multitool sendo exibido na tela.
- Ao ligar o Multitool, uma tela cinza será exibida antes de entrar na tela de opções.
- Verifique a mensagem exibida na tela cinza para identificar o tipo de memória da TV Box.
- Se você visualizar "rknand" no início do texto, isso indica que a memória é do tipo NAND.
- OPCIONAL : você pode fazer um backup do firmware existente com a opção de menu " Flash de backup".
- Caso queria restaura a TV Box com a ROM de fábrica.
- Escolha a opção "Install Armbian via steP-nand" no menu e espere a ISO ser gravada.
- Após a conclusão da gravação da ISO, navegue até o menu e selecione a opção "Shutdown".
- Aguarde até que a TV Box seja desligada completamente.
- Desconecte o cabo de alimentação da TV Box.
- Remova o cartão microSD da TV Box.
- Conecte a TV Box novamente ao cabo de alimentação e aguarde até que ela ligue.
- Verifique se tudo ocorreu corretamente observando o pisca-pisca do LED azul e uma tela preta indicando o carregamento do sistema.
- Após o carregamento, será solicitada a inserção de uma senha de root.
- Em seguida, escolha a "shell padrão" de sua preferência entre as opções bash e zsh.
- Digite o nome de usuário e, em seguida, a senha. Confirme o nome de usuário mais uma vez.
- Após isso, a área de trabalho do Armbian será aberta na tela.
- Para fazer os ajustes finais, clique em "Applications" localizado no canto superior esquerdo da tela.
- Procure por "Terminal Emulator" e clique nessa opção para abrir o terminal do Armbian.
- No terminal aberto, digite o comando "sudo rk322x-config" para realizar algumas configurações na TV Box.
- Insira a senha root quando solicitado e uma tela cinza será exibida.
- Na primeira tela, "Board configuration", defina o processador da TV Box selecionando "RK3228A" ou "RK3228B", em seguida, clique em "OK".
- Em seguida, selecione a opção "NAND" como tipo de memória e clique em "OK".
- Será perguntado a frequência em MHz do DDR. Selecione "DDR2 330MHz" para memória DDR2 ou "DDR3 660MHz" para memória DDR3 e clique em "OK".
- Depois, selecione a opção de configuração do LED, como "led-conf2 (R329q, MXQ-RK3229)". Se não tiver certeza, verifique essa informação abrindo a TV Box.
- Escolha o módulo Wi-Fi como "ssv6051".
- Para reiniciar a TV Box, digite o comando "sudo reboot" ou "reboot" no terminal e aguarde até que a reinicialização seja concluída.
- Se a área de trabalho do Armbian for aberta normalmente, a TV Box está pronta para uso.

