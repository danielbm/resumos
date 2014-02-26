Red Hat: Serviços de Infraestrutura
===================================


# Gerenciando os Serviços do Sistema

Para iniciar, reiniciar, parar, ou checar o status de um serviço, digite:

        service name action

em `name` é o nome do serviço que está administrando e `action` é a ação que deseja realizar. Esses comandos são providos por um utilitário chamado `systemctl`.

## Listando Serviços

Comandos:

        systemctl list-units --type service

        systemctl list-units --type service --all


## Desligando o Sistema

Comandos:

        systemctl poweroff
        
        systemctl halt
        
        systemctl reboot
        
        systemctl hibernate


