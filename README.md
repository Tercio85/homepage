# Passo a passo para criar um script em Linux, que instala o Apache2 e exibe uma página HTML simples:

## Para criar um script primeiro devemos criar um novo arquivo comum, com o comando: 

```Bash
sudo nano script.sh
```

## Após declare que isso é um script que deve ser executado com o Bash. Utilizando o comando: 
```Bash
#! /bin/bash
```

## Atualizar a lista de pacotes do sistema para garantir que tenhamos as versões mais recentes disponíveis, realizando o comando: 
```Bash
sudo apt update
```

## Em seguida realizar o comando para instalar o apache2, junto com o comando para confirmar a instalação, que é: 
```Bash
sudo apt install apache2 -y
```

## Crie um diretório específico para sua página html, com o comando:
```Bash
sudo mkdir /var/www/homepage
```

## Em seguida crie uma página html usando os comandos: 
```echo```  e  ```sudo tee``` para criar um arquivo index.html no diretório desejado (/var/www/html/ ou /var/www/homepage/);

## Agora ajuste as permissões com os seguintes comandos: 
```Bash
sudo chown -R www-data:www-data /var/www/homepage
```
```Bash
sudo chmod -R 755 /var/www/homepage```

## Reinicie o Apache:
```Bash
sudo systemctl restart apache2
```

## Após torne o script executável: 
```Bash
chmod +x instala_apache.sh```

## Agora é só acessar o IP do seu servidor no navegador para ver sua página HTML.
