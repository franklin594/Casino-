--[[
##########################################
#         Script Base Game Guardian       #
#           Criado por: SEU_NOME          #
#     Github: github.com/SEU_USUARIO      #
##########################################
]]

-- Informações básicas
local nomeScript = "Meu Script GG Online"
local versao = "1.0.0"

-- Boas-vindas
gg.alert(nomeScript .. "\nVersão: " .. versao .. "\n\nSeja bem-vindo!")

-- Função principal do menu
function menuPrincipal()
    local opcao = gg.choice({
        "➤ Função 1 (Exemplo)",
        "➤ Função 2 (Exemplo)",
        "➤ Sair"
    }, nil, nomeScript .. "\nEscolha uma opção:")

    if opcao == 1 then
        funcao1()
    elseif opcao == 2 then
        funcao2()
    elseif opcao == 3 then
        gg.alert("Saindo...")
        os.exit()
    end
end

-- Funções de exemplo
function funcao1()
    gg.alert("Função 1 ativada!")
    -- Aqui vai seu código para busca ou alteração de valores
end

function funcao2()
    gg.alert("Função 2 ativada!")
    -- Aqui vai outro código
end

-- Loop do script
while true do
    if gg.isVisible(true) then
        gg.setVisible(false)
        menuPrincipal()
    end
end
