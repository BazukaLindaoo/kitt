-- LocalScript: Tela de Loading "KitK4t Hub X"
-- Coloque este LocalScript dentro de StarterPlayerScripts ou StarterGui (PlayerGui será usado)
local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local RunService = game:GetService("RunService")

local player = Players.LocalPlayer
local PLAYER_GUI = player:WaitForChild("PlayerGui")

-- Configurações
local RED = Color3.fromRGB(200, 0, 0)
local BLACK = Color3.fromRGB(0, 0, 0)
local DURATION = 3 -- segundos

-- Criar ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "KitK4tLoadingGui"
screenGui.ResetOnSpawn = false
screenGui.Parent = PLAYER_GUI

-- Fundo preto full-screen
local bg = Instance.new("Frame")
bg.Name = "Background"
bg.Size = UDim2.fromScale(1, 1)
bg.Position = UDim2.fromScale(0, 0)
bg.BackgroundColor3 = BLACK
bg.BorderSizePixel = 0
bg.Parent = screenGui

-- Container central
local container = Instance.new("Frame")
container.Name = "Container"
container.Size = UDim2.new(0.6, 0, 0.34, 0)
container.AnchorPoint = Vector2.new(0.5, 0.5)
container.Position = UDim2.fromScale(0.5, 0.5)
container.BackgroundTransparency = 1
container.Parent = bg

-- Título
local title = Instance.new("TextLabel")
title.Name = "Title"
title.Size = UDim2.new(1, 0, 0.5, 0)
title.Position = UDim2.new(0, 0, 0, 0)
title.BackgroundTransparency = 1
title.Text = "KitK4t Hub X"
title.Font = Enum.Font.GothamBold
title.TextSize = 48
title.TextScaled = true
title.TextColor3 = RED
title.TextStrokeTransparency = 0 -- contorno visível
title.TextStrokeColor3 = BLACK
title.TextWrapped = true
title.Parent = container

-- Subtítulo
local subtitle = Instance.new("TextLabel")
subtitle.Name = "Subtitle"
subtitle.Size = UDim2.new(1, 0, 0.18, 0)
subtitle.Position = UDim2.new(0, 0, 0.52, 0)
subtitle.BackgroundTransparency = 1
subtitle.Text = "WxDeveloper, BazukaLindaoo, Lusquinha_067"
subtitle.Font = Enum.Font.Gotham
subtitle.TextSize = 20
subtitle.TextScaled = true
subtitle.TextColor3 = RED
subtitle.TextStrokeTransparency = 0
subtitle.TextStrokeColor3 = BLACK
subtitle.TextWrapped = true
subtitle.Parent = container

-- Barra de progresso (fundo)
local barBackground = Instance.new("Frame")
barBackground.Name = "BarBackground"
barBackground.Size = UDim2.new(1, 0, 0.15, 0)
barBackground.Position = UDim2.new(0, 0, 0.76, 0)
barBackground.BackgroundColor3 = BLACK
barBackground.BorderColor3 = RED
barBackground.BorderSizePixel = 2
barBackground.Parent = container

local barUICorner = Instance.new("UICorner")
barUICorner.Parent = barBackground
barUICorner.CornerRadius = UDim.new(0, 8)

-- Barra de preenchimento (inicialmente vazia)
local barFill = Instance.new("Frame")
barFill.Name = "BarFill"
barFill.Size = UDim2.new(0, 0, 1, 0)
barFill.Position = UDim2.new(0, 0, 0, 0)
barFill.BackgroundColor3 = RED
barFill.BorderSizePixel = 0
barFill.Parent = barBackground

local fillUICorner = Instance.new("UICorner")
fillUICorner.Parent = barFill
fillUICorner.CornerRadius = UDim.new(0, 8)

-- Texto percentual central na barra
local percent = Instance.new("TextLabel")
percent.Name = "Percent"
percent.Size = UDim2.fromScale(1, 1)
percent.Position = UDim2.fromScale(0, 0)
percent.BackgroundTransparency = 1
percent.Text = "0%"
percent.Font = Enum.Font.Gotham
percent.TextSize = 18
percent.TextScaled = true
percent.TextColor3 = RED
percent.TextStrokeTransparency = 0
percent.TextStrokeColor3 = BLACK
percent.Parent = barBackground

-- Tween para preencher barra
local tweenInfo = TweenInfo.new(DURATION, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
local goal = {Size = UDim2.new(1, 0, 1, 0)}
local tween = TweenService:Create(barFill, tweenInfo, goal)
tween:Play()

-- Atualizar percentual em tempo real
local startTime = tick()
local conn
conn = RunService.Heartbeat:Connect(function()
    local elapsed = math.clamp(tick() - startTime, 0, DURATION)
    local pct = math.floor((elapsed / DURATION) * 100 + 0.5)
    percent.Text = tostring(pct) .. "%"
    if elapsed >= DURATION then
        conn:Disconnect()
    end
end)

-- Ao terminar, esperar 0.15s e remover GUI
tween.Completed:Connect(function()
    percent.Text = "100%"
    wait(0.15)
    screenGui:Destroy()
end)


delay(3, function()
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/wx-sources/unixLibraryy/refs/heads/main/Redzhubui.txt"))()
local Window = redzlib:MakeWindow({
  Title = "KitK4t Hub X | Nova Era",
  SubTitle = "Era Atual: X",
  SaveFolder = "testando | v1"
})

Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://0", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})

local Tab1 = Window:MakeTab({"Credits", "info"})

Tab1:AddDiscordInvite({
    Name = "KitK4t Hub X | Nova Era",
    Description = "KitKat Nova Era : X",
    Logo = "rbxassetid://0",
    Invite = "https://discord.gg/C6n3FyaB8D",
})

local Section = Tab1:AddSection({"Credits"})

local Paragraph = Tab1:AddParagraph({"Criador", "Bazuka\nWx\nLuscaa\nChatGPT"})

local Paragraph = Tab1:AddParagraph({"Versão", "Versão X"})

if identifyexecutor then
local Paragraph = Tab1:AddParagraph({"Executor", identifyexecutor()})
else
warn("nao deu pra identificar o exc!")
end

local Paragraph = Tab1:AddParagraph({"Era Atual: X"})

local Tab2 = Window:MakeTab({"Autofarm / Eventos", "fun"})

local Section = Tab2:AddSection({" "})

local Tab3 = Window:MakeTab({"Som de tool", "Home"})

local Section = Tab3:AddSection({"PRECISA EQUIPAR A GUITARRA E VIOLÃO PRA FUNCIONAR"})
Tab3:AddButton({
		Name = "SOM DE GUITARRA", 
		Callback = function()
			local args = {
	"ElectricGuitarMusic1"
}
game:GetService("Players").LocalPlayer.Character:WaitForChild("ElectricGuitar"):WaitForChild("ToolSound"):FireServer(unpack(args))
		end
	})

Tab3:AddButton({
		Name = "SOM DE VIOLÃO", 
		Callback = function()
			local args = {
	"GuitarMusic1"
}
game:GetService("Players").LocalPlayer:WaitForChild("Backpack"):WaitForChild("Guitar"):WaitForChild("ToolSound"):FireServer(unpack(args))
		end
	})





local TrollTab = Window:MakeTab({ Title = "Anime + Rgb", Icon = "rbxassetid://13364900349" })

local SpamTab = Window:MakeTab({ Title = "Spam", Icon = "mousepointer2" })

do

SpamTab:AddSection({Name = "Spam"})

SpamTab:AddSection({Name = "SPAM DE JATOS"})

SpamTab:AddParagraph({"JATO SPAM"})

local Players = game:GetService("Players")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

local player = Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local originalPosition = player.Character and player.Character:FindFirstChild("HumanoidRootPart") and player.Character.HumanoidRootPart.Position

local clickDetector = Workspace.WorkspaceCom["001_Airport"].AirportHanger["001_JetCloneButton"].Button.ClickDetector
local jetStorage = Workspace.WorkspaceCom["001_Airport"].AirportHanger["001_JetStorage"]
local buttonPosition = Vector3.new(498.99, -19.52, 278.73)
local targetPosition = Vector3.new(-26.20, 98.02, 17.45)
local voidPosition = Vector3.new(0, -1000, 0)
local selectedPlayer = nil

local running1 = false
local running2 = false
local loopConnection1, loopConnection2

local function getFirstPart(jet)
    for _, part in ipairs(jet:GetDescendants()) do
        if part:IsA("BasePart") then
            return part
        end
    end
    return nil
end

local function getDistance(pos1, pos2)
    return (pos1 - pos2).Magnitude
end

local function waitForNewJet(existingJets)
    local maxAttempts = 10
    local attempt = 0
    while (running1 or running2) and attempt < maxAttempts do
        for _, jet in ipairs(jetStorage:GetChildren()) do
            if jet:IsA("Model") and not existingJets[jet] then
                return jet
            end
        end
        attempt = attempt + 1
        RunService.Heartbeat:Wait()
    end
    return nil
end

local function teleportAndStabilizeJet(jet, position)
    local primaryPart = getFirstPart(jet)
    if not primaryPart then
        return false
    end

    local maxAttempts = 5
    local attempt = 0
    while attempt < maxAttempts do
        pcall(function()
            jet.PrimaryPart = primaryPart
        end)
        primaryPart.Anchored = false
        task.wait(0.3)
        pcall(function()
            jet:SetPrimaryPartCFrame(CFrame.new(position) * CFrame.Angles(0, math.rad(90), 0))
            task.wait(0.5)
            primaryPart.Velocity = Vector3.new(0, 0, 0)
            primaryPart.RotVelocity = Vector3.new(0, 0, 0)
        end)
        if (jet.PrimaryPart and (jet.PrimaryPart.Position - position).Magnitude < 5) then
            return true
        end
        attempt = attempt + 1
        task.wait(0.5)
    end
    return false
end

local function showNotification(playerName, playerImage)
    local notification = Instance.new("ScreenGui")
    notification.Parent = playerGui

    local frame = Instance.new("Frame")
    frame.Size = UDim2.new(0, 200, 0, 100)
    frame.Position = UDim2.new(0.5, -100, 0.5, -50)
    frame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    frame.Parent = notification

    local image = Instance.new("ImageLabel")
    image.Size = UDim2.new(0, 50, 0, 50)
    image.Position = UDim2.new(0, 10, 0, 25)
    image.BackgroundTransparency = 1
    image.Image = playerImage or "rbxasset://textures/ui/GuiImagePlaceholder.png"
    image.Parent = frame

    local text = Instance.new("TextLabel")
    text.Size = UDim2.new(0, 130, 0, 50)
    text.Position = UDim2.new(0, 70, 0, 25)
    text.BackgroundTransparency = 1
    text.TextColor3 = Color3.new(1, 1, 1)
    text.Text = "Player: " .. (playerName or "Unidentified")
    text.Font = Enum.Font.SourceSansBold
    text.TextSize = 16
    text.Parent = frame

    task.delay(3, function()
        notification:Destroy()
    end)
end

local function startLoop1()
    if running1 then return end
    running1 = true

    for _, jet in ipairs(jetStorage:GetChildren()) do
        if jet:IsA("Model") then
            local primaryPart = getFirstPart(jet)
            if primaryPart and getDistance(primaryPart.Position, buttonPosition) < 50 then
                teleportAndStabilizeJet(jet, voidPosition)
                task.wait(0.5)
            end
        end
    end

    loopConnection1 = RunService.Heartbeat:Connect(function()
        if not running1 then return end

        local existingJets = {}
        for _, jet in ipairs(jetStorage:GetChildren()) do
            existingJets[jet] = true
        end

        fireclickdetector(clickDetector)
        player.Character:SetPrimaryPartCFrame(CFrame.new(buttonPosition))
        task.wait(0.5)

        local newJet = waitForNewJet(existingJets)
        if newJet then
            while not teleportAndStabilizeJet(newJet, targetPosition) do
                task.wait(0.5)
            end
            task.wait(0.5)
        else
            task.wait(0.5)
        end
    end)
end

local function stopLoop1()
    running1 = false
    if loopConnection1 then
        loopConnection1:Disconnect()
        loopConnection1 = nil
    end
    if originalPosition and player.Character then
        player.Character:SetPrimaryPartCFrame(CFrame.new(originalPosition))
    end
end

local function startLoop2()
    if running2 or not selectedPlayer or not selectedPlayer.Character then return end
    running2 = true

    for _, jet in ipairs(jetStorage:GetChildren()) do
        if jet:IsA("Model") then
            local primaryPart = getFirstPart(jet)
            if primaryPart and getDistance(primaryPart.Position, buttonPosition) < 50 then
                teleportAndStabilizeJet(jet, voidPosition)
                task.wait(0.5)
            end
        end
    end

    loopConnection2 = RunService.Heartbeat:Connect(function()
        if not running2 then return end

        local existingJets = {}
        for _, jet in ipairs(jetStorage:GetChildren()) do
            existingJets[jet] = true
        end

        fireclickdetector(clickDetector)
        player.Character:SetPrimaryPartCFrame(CFrame.new(buttonPosition))
        task.wait(0.5)

        local newJet = waitForNewJet(existingJets)
        if newJet and selectedPlayer.Character and selectedPlayer.Character:FindFirstChild("HumanoidRootPart") then
            while not teleportAndStabilizeJet(newJet, selectedPlayer.Character.HumanoidRootPart.Position) do
                task.wait(0.5)
            end
            task.wait(0.5)
        else
            task.wait(0.5)
        end
    end)
end

local function stopLoop2()
    running2 = false
    if loopConnection2 then
        loopConnection2:Disconnect()
        loopConnection2 = nil
    end
    if originalPosition and player.Character then
        player.Character:SetPrimaryPartCFrame(CFrame.new(originalPosition))
    end
end

SpamTab:AddTextBox({
    Name = "Player Name",
    Description = "Enter the player's name to start spamming them",
    PlaceholderText = "Type Here...",
    Callback = function(Value)
        local input = Value:lower()
        if input ~= "" then
            for _, plr in ipairs(Players:GetPlayers()) do
                if plr.Name:lower():sub(1, #input) == input then
                    selectedPlayer = plr
                    showNotification(plr.Name, "rbxthumb://id=" .. plr.UserId .. "?width=50&height=50")
                    break
                end
            end
        else
            selectedPlayer = nil
            showNotification("Unidentified", nil)
        end
    end
})

SpamTab:AddButton({
    Name = "COMEÇAR SPAM PLAYER",
    Callback = function()
        startLoop2()
    end
})

SpamTab:AddButton({
    Name = "PARAR SPAM PLAYER",
    Callback = function()
        stopLoop2()
    end
})

SpamTab:AddSection({"LOCAL"})

SpamTab:AddButton({
    Name = "COMEÇAR SPAM",
    Callback = function()
        startLoop1()
    end
})

SpamTab:AddButton({
    Name = "PARAR SPAM",
    Callback = function()
        stopLoop1()
    end
})

SpamTab:AddParagraph({"VAI SPAMMAR EM LOCAL."})

end

SpamTab:AddSection({"SPAM DE BOMBAS"})
SpamTab:AddToggle({
    Name = "SPAM DE BOMBAS NA ÁREA SECRETA",
    Default = false,
    Callback = function(Value)
        if Value then
            BombActive = true

            local Player = game.Players.LocalPlayer
            local Character = Player.Character or Player.CharacterAdded:Wait()
            local RootPart = Character:WaitForChild("HumanoidRootPart")
            local WorkspaceService = game:GetService("Workspace")
            local ReplicatedStorage = game:GetService("ReplicatedStorage")
            local Bomb = WorkspaceService:WaitForChild("WorkspaceCom"):WaitForChild("001_CriminalWeapons"):WaitForChild("GiveTools"):WaitForChild("Bomb")

            task.spawn(function()
                while BombActive do
                    if Bomb and RootPart then
                        RootPart.CFrame = Bomb.CFrame
                        fireclickdetector(Bomb.ClickDetector) 
                        task.wait(0.00001) 
                    else
                        task.wait(0.0001) 
                    end
                end
            end)

            task.spawn(function()
                while BombActive do
                    if Bomb and RootPart then
                        local VirtualInputManager = game:GetService("VirtualInputManager")
                        VirtualInputManager:SendMouseButtonEvent(500, 500, 0, true, game, 0) 
                        task.wait(1.5)
                        VirtualInputManager:SendMouseButtonEvent(500, 500, 0, false, game, 0) 

                        local args = {
                            [1] = "Bomb" .. Player.Name 
                        }
                        ReplicatedStorage:WaitForChild("RE"):WaitForChild("1Blo1wBomb1sServe1r"):FireServer(unpack(args))
                    end
                    task.wait(1.5) 
                end
            end)
        else
            BombActive = false
        end
    end
})

local ToolsTab = Window:MakeTab({"Tools", "backpack"})

local SectionDupl = ToolsTab:AddSection({
Name = "Duplicate Laptops"
})
ToolsTab:AddButton({
Name = "Duplicate Laptops (Required for Some Things)",
Callback = function()
-- Função para simular clique normal
local function clickNormally(object)
local clickDetector = object:FindFirstChildWhichIsA("ClickDetector")
if clickDetector then
fireclickdetector(clickDetector)
end
end

-- Encontrar o laptop
local laptop = workspace:FindFirstChild("WorkspaceCom")
if laptop then
laptop = laptop:FindFirstChild("001_GiveTools")
if laptop then
laptop = laptop:FindFirstChild("Laptop")
end
end

if laptop then
local player = game.Players.LocalPlayer
local character = player.Character
if character and character:FindFirstChild("HumanoidRootPart") then
local startTime = tick()  -- Marca o tempo de início
while tick() - startTime < 60 do  -- Loop por 60 segundos
-- Teleportar para o laptop
character.HumanoidRootPart.CFrame = laptop.CFrame
-- Clicar continuamente
clickNormally(laptop)
-- Delay para evitar crash
task.wait(0.25)
end

-- Desequipar todas as ferramentas, mantendo-as no inventário    
    local backpack = player:FindFirstChildOfClass("Backpack")    
    if backpack then    
        for _, tool in ipairs(character:GetChildren()) do    
            if tool:IsA("Tool") then    
                tool.Parent = backpack  -- Move a ferramenta da mão para o inventário    
            end    
        end    
    end    

    print("Parou de clicar após 60 segundos e ferramentas foram desequipadas.")    
else    
    warn("HumanoidRootPart não encontrado.")    
end

else
warn("Laptop não encontrado.")
end
end
})

-- Referências aos remotes
local cleartoolremote = game:GetService("ReplicatedStorage").RE:FindFirstChild("1Clea1rTool1s")
local picktoolremote = game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l")

-- Seção de controle de itens
local Section = ToolsTab:AddSection({
Name = "Items Control"
})

-- Botão para limpar todas as ferramentas
ToolsTab:AddButton({
Name = "Clear All Tools",
Callback = function()
local args = {
[1] = "ClearAllTools"
}
game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Clea1rTool1s"):FireServer(unpack(args))
end
})

-- Seção para equipar itens
Section = ToolsTab:AddSection({
Name = "Equip Items"
})

-- Botão para equipar todos os itens
ToolsTab:AddButton({
Name = "Equipar todos os itens",
Callback = function()
for _, tool in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
if tool:IsA("Tool") then
tool.Parent = game.Players.LocalPlayer.Character
end
end
end
})

-- Seção para Testes
Section = ToolsTab:AddSection({
Name = "Super Aura Things/Tools"
})

-- Botão para Super Aura Smoke
ToolsTab:AddButton({
Name = "Super Aura Smoke [ NEW ! ]",
Description = "A aura vai aparecer se vc segurar a tela, aí a fumaça vai aparecendo!",
Callback = function()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer

-- Caminho do FireX
local fireXPath = workspace:FindFirstChild("WorkspaceCom")
and workspace.WorkspaceCom:FindFirstChild("001_GiveTools")
and workspace.WorkspaceCom["001_GiveTools"]:FindFirstChild("FireX")

local nametools = "crystal nazi lel"
local oldcframe = LocalPlayer.Character.HumanoidRootPart.CFrame
local attempts = 57
local delayBetweenClicks = 0.3

-- Grip e Handle
local gripBase = CFrame.new(-0.290086746, 0.0755810738, -0.0109872818, 0.0439560413, 0.509705901, -0.859225094, -0.0591450632, -0.857220173, -0.511542261, -0.997281134, 0.0733042806, -0.00753343105)
local handleOffset = CFrame.new(2, 1, -3)

-- Velocidade absurda de rotação (sempre)
local rotSpeed = math.rad(3600) -- 3600°/s

-- Função de clique na ferramenta
local function clickTool(object)
local clickDetector = object:FindFirstChildWhichIsA("ClickDetector")
if clickDetector then
fireclickdetector(clickDetector)
end
end

-- Configura Grip e Handle
local function setupTool(tool)
tool.Grip = gripBase
tool.Name = nametools

local handle = tool:FindFirstChild("Handle")    
if handle then    
    local weld = handle:FindFirstChildWhichIsA("Motor6D")    
    if weld then weld:Destroy() end    

    -- HandleOffset fixo    
    RunService.RenderStepped:Connect(function()    
        if handle.Parent == LocalPlayer.Character then    
            handle.CFrame = LocalPlayer.Character.HumanoidRootPart.CFrame * handleOffset    
        end    
    end)    
end    

tool.Parent = LocalPlayer.Character

end

-- Rotação contínua infinita
RunService.RenderStepped:Connect(function(deltaTime)
local hrp = LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
if hrp then
hrp.CFrame = hrp.CFrame * CFrame.Angles(0, rotSpeed * deltaTime, 0)
end
end)

-- Função de duplicação do FireX
local function dupeToolsFireX(fireXPath)
if not fireXPath then
warn("FireX não encontrado.")
return
end

local hrp = LocalPlayer.Character:FindFirstChild("HumanoidRootPart")    
if not hrp then return end    

hrp.CFrame = fireXPath.CFrame    

for i = 1, attempts do    
    clickTool(fireXPath)    
    task.wait(delayBetweenClicks)    

    local tool = LocalPlayer.Backpack:FindFirstChild("FireX")    
    if tool then    
        setupTool(tool)    
    end    
end    

hrp.CFrame = oldcframe

end

-- Executa o dupe
dupeToolsFireX(fireXPath)
end
})

local SectionToolW = ToolsTab:AddSection({
Name = "Tool Writer (doesnt support more than 10 letters)"
})

ToolsTab:AddButton({
Name = "Tool Writer (10 Letters)",
Callback = function()
if getgenv()._Running then
warn("Already running")
return
end
getgenv()._Running = true

local Players = game:GetService("Players")
local CoreGui = game:GetService("CoreGui")
local UserInputService = game:GetService("UserInputService")
local player = Players.LocalPlayer

local CHAR_MAP = {
["A"] = {"01110","10001","10001","11111","10001","10001","10001"},
["B"] = {"11110","10001","10001","11110","10001","10001","11110"},
["C"] = {"01110","10001","10000","10000","10000","10001","01110"},
["D"] = {"11110","10001","10001","10001","10001","10001","11110"},
["E"] = {"11111","10000","10000","11110","10000","10000","11111"},
["F"] = {"11111","10000","10000","11110","10000","10000","10000"},
["G"] = {"01110","10001","10000","10111","10001","10001","01110"},
["H"] = {"10001","10001","10001","11111","10001","10001","10001"},
["I"] = {"111","010","010","010","010","010","111"},
["J"] = {"00111","00010","00010","00010","10010","10010","01100"},
["K"] = {"10001","10010","10100","11000","10100","10010","10001"},
["L"] = {"10000","10000","10000","10000","10000","10000","11111"},
["M"] = {"10001","11011","10101","10101","10001","10001","10001"},
["N"] = {"10001","11001","10101","10011","10001","10001","10001"},
["O"] = {"01110","10001","10001","10001","10001","10001","01110"},
["P"] = {"11110","10001","10001","11110","10000","10000","10000"},
["Q"] = {"01110","10001","10001","10001","10101","10010","01101"},
["R"] = {"11110","10001","10001","11110","10100","10010","10001"},
["S"] = {"01111","10000","10000","01110","00001","00001","11110"},
["T"] = {"11111","00100","00100","00100","00100","00100","00100"},
["U"] = {"10001","10001","10001","10001","10001","10001","01110"},
["V"] = {"10001","10001","10001","10001","10001","01010","00100"},
["W"] = {"10001","10001","10001","10101","10101","11011","10001"},
["X"] = {"10001","01010","00100","00100","01010","10001","10001"},
["Y"] = {"10001","10001","10001","01010","00100","00100","00100"},
["Z"] = {"11111","00001","00010","00100","01000","10000","11111"},
[" "] = {"00000","00000","00000","00000","00000","00000","00000"},
}

local screenGui = Instance.new("ScreenGui")
screenGui.Name = "TextToolGUI"
screenGui.Parent = CoreGui
screenGui.ResetOnSpawn = false

local mainFrame = Instance.new("Frame", screenGui)
mainFrame.Size = UDim2.new(0, 250, 0, 120)
mainFrame.Position = UDim2.new(0.5, -125, 0.5, -60)
mainFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
mainFrame.BorderSizePixel = 0
Instance.new("UICorner", mainFrame).CornerRadius = UDim.new(0, 10)

local title = Instance.new("TextLabel", mainFrame)
title.Size = UDim2.new(1, 0, 0, 30)
title.BackgroundTransparency = 1
title.Text = "Text Former"
title.Font = Enum.Font.GothamBold
title.TextSize = 16
title.TextColor3 = Color3.fromRGB(255, 50, 50)

local textBox = Instance.new("TextBox", mainFrame)
textBox.Size = UDim2.new(0.9, 0, 0, 30)
textBox.Position = UDim2.new(0.05, 0, 0, 40)
textBox.PlaceholderText = "Type here..."
textBox.Text = ""
textBox.TextSize = 14
textBox.Font = Enum.Font.Gotham
textBox.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
textBox.TextColor3 = Color3.new(1,1,1)
Instance.new("UICorner", textBox).CornerRadius = UDim.new(0, 6)

local button = Instance.new("TextButton", mainFrame)
button.Size = UDim2.new(0.9, 0, 0, 30)
button.Position = UDim2.new(0.05, 0, 0, 80)
button.Text = "Form Text"
button.Font = Enum.Font.GothamBold
button.TextSize = 14
button.BackgroundColor3 = Color3.fromRGB(255, 50, 50)
button.TextColor3 = Color3.new(1,1,1)
Instance.new("UICorner", button).CornerRadius = UDim.new(0, 6)

local function getTools()
local tools = {}
for _, c in ipairs({player.Backpack, player.Character}) do
for _, tool in ipairs(c:GetChildren()) do
if tool:IsA("Tool") then
table.insert(tools, tool)
end
end
end
return tools
end

local function formText(text)
local tools = getTools()
local gripMap = {}
local startPos = Vector3.new(0, -5, 0)
local pixelSize = Vector3.new(1.2, 1.2, 0)
local toolIndex = 1
local offsetX = 0

for i = 1, #text do    
    local char = text:sub(i,i):upper()    
    local map = CHAR_MAP[char]    
    if map then    
        for y = 1, #map do    
            for x = 1, #map[y] do    
                if map[y]:sub(x,x) == "1" then    
                    local tool = tools[toolIndex]    
                    if tool then    
                        gripMap[tool] = CFrame.new(    
                            startPos.X + (offsetX + x - 1) * pixelSize.X,    
                            startPos.Y + (y - 1) * pixelSize.Y,    
                            startPos.Z    
                        )    
                        toolIndex += 1    
                    end    
                end    
            end    
        end    
        offsetX += #map[1] + 1    
    end    
end    

for tool, grip in pairs(gripMap) do    
    tool.Grip = grip    
    tool.Parent = player.Character    
end

end

button.MouseButton1Click:Connect(function()
if textBox.Text ~= "" then
formText(textBox.Text)
end
end)

do
local dragging, dragInput, dragStart, startPos
mainFrame.InputBegan:Connect(function(input)
if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
dragging = true
dragStart = input.Position
startPos = mainFrame.Position

input.Changed:Connect(function()    
            if input.UserInputState == Enum.UserInputState.End then    
                dragging = false    
            end    
        end)    
    end    
end)    

mainFrame.InputChanged:Connect(function(input)    
    if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then    
        dragInput = input    
    end    
end)    

UserInputService.InputChanged:Connect(function(input)    
    if input == dragInput and dragging then    
        local delta = input.Position - dragStart    
        mainFrame.Position = UDim2.new(    
            startPos.X.Scale, startPos.X.Offset + delta.X,    
            startPos.Y.Scale, startPos.Y.Offset + delta.Y    
        )    
    end    
end)

end

getgenv()._Running = false
end
})

local Tab = Window:MakeTab({"Teleports", "tp"}) 

local Section = Tab:AddSection({
    Name = "Teleports"
})

local teleportButtons = {
    {"Tp hotel", CFrame.new(192, 4, 272)},
    {"Tp centro", CFrame.new(136, 4, 117)},
    {"Tp área dos criminosos", CFrame.new(-119, -28, 235)},
    {"Tp casa abandonada", CFrame.new(986, 4, 63)},
    {"Tp agency portal", CFrame.new(672, 4, -296)},
    {"Tp esconderijo", CFrame.new(505, -75, 143)},
    {"Tp brookhaven doge school", CFrame.new(-312, 4, 211)},
    {"Tp starbuckscoffee", CFrame.new(-97.12, 4.65, 254.99)}
}
for _, btn in ipairs(teleportButtons) do
    Tab:AddButton({
        btn[1],
        function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = btn[2]
        end
    })
end


local NamesTab = Window:MakeTab({"Nomes V2", "Paper"})

local isNameActive = false
local isBioActive = false

local SectionRGBName = NamesTab:AddSection({
    Name = "Name"
})

NamesTab:AddToggle({
    Name = "Name RGB",
    Description = "Make the Name colorful",
    Default = false,
    Callback = function(value)
        isNameActive = value
    end
})

local SectionRGBBio = NamesTab:AddSection({
    Name = "Bio"
})

NamesTab:AddToggle({
    Name = "Bio RGB",
    Description = "Make the Bio colorful",
    Default = false,
    Callback = function(value)
        isBioActive = value
    end
})

local vibrantColors = {
    Color3.fromRGB(255, 0, 0),
    Color3.fromRGB(0, 255, 0),
    Color3.fromRGB(0, 0, 255),
    Color3.fromRGB(255, 255, 0),
    Color3.fromRGB(255, 0, 255),
    Color3.fromRGB(0, 255, 255),
    Color3.fromRGB(255, 165, 0),
    Color3.fromRGB(128, 0, 128),
    Color3.fromRGB(255, 20, 147)
}

spawn(function()
    while true do
        if isNameActive then
            local randomColor = vibrantColors[math.random(#vibrantColors)]
            local args = {
                [1] = "PickingRPNameColor",
                [2] = randomColor
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1RPNam1eColo1r"):FireServer(unpack(args))
        end
        wait(0.25)
    end
end)

spawn(function()
    while true do
        if isBioActive then
            local randomColor = vibrantColors[math.random(#vibrantColors)]
            local args = {
                [1] = "PickingRPBioColor",
                [2] = randomColor
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1RPNam1eColo1r"):FireServer(unpack(args))
        end
        wait(0.7)
    end
end)

local SectionNames = NamesTab:AddSection({
    Name = "Custom Names by ChatGPT"
})

local names = {
    {"AN0NYMUS", " AN0NYMUS "},
    {"REW0RK X", " REW0RK X "},
    {"AM0NG US", " AM0NG US "},
    {"TUB3RS93", " TUB3RS 93 "},
    {"C00LK1D", " C00 LK1D "},
    {"GAM3 ATTACKED BY X HUB", " GAM3 ATTACKED BY X HUB "},
    {"X HUB", " X HUB "},
    {"1NC0MU", " 1NC0MU "},
    {"GAM3 HIJACKED BY ERA X", " GAM3 HIJACKED BY ERA X "},
    {"B4ZUC4", " B4ZUC4 "},
    {"1X1X1X1", " 1X1X1X1 "},
    {"VOIDH4CK", " VOIDH4CK "},
    {"R3B00T X", " R3B00T X "},
    {"CR4SH0R", " CR4SH0R "},
    {"XTR3ME H4CKER", " XTR3ME H4CKER "},
    {"D3STR0YER", " D3STR0YER "},
    {"N1GHTH4WK", " N1GHTH4WK "},
    {"GL1TCH M4STER", " GL1TCH M4STER "},
    {"H1J4CK3D BY ERA X", " H1J4CK3D BY ERA X "},
    {"B0MB3R", " B0MB3R "},
    {"INF1N1TY H4CK", " INF1N1TY H4CK "},
    {"SHADOW STR1K3R", " SHADOW STR1K3R "},
    {"Z3R0 C00L", " Z3R0 C00L "},
    {"X HUB ATTACK", " X HUB ATTACK "},
    {"L33T INV4S10N", " L33T INV4S10N "},
    {"G4M3 H4CK3R", " G4M3 H4CK3R "},
    {"CRYPT1C", " CRYPT1C "},
    {"N0 SC0P3 H4CK", " N0 SC0P3 H4CK "}
}

for _, name in ipairs(names) do
    NamesTab:AddButton({
        Name = name[1],
        Callback = function()
            game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName", name[2])
        end
    })
end
TrollTab:AddSection({ "Black Hole" })
TrollTab:AddButton({
    Name = "Black Hole",
    Description = " Ativando isso você puxa Parts até o seu personagem",
    Callback = function()
        local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer
local Workspace = game:GetService("Workspace")

local angle = 1
local radius = 10
local blackHoleActive = false

local function setupPlayer()
    local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

    local Folder = Instance.new("Folder", Workspace)
    local Part = Instance.new("Part", Folder)
    local Attachment1 = Instance.new("Attachment", Part)
    Part.Anchored = true
    Part.CanCollide = false
    Part.Transparency = 1

    return humanoidRootPart, Attachment1
end

local humanoidRootPart, Attachment1 = setupPlayer()

if not getgenv().Network then
    getgenv().Network = {
        BaseParts = {},
        Velocity = Vector3.new(14.46262424, 14.46262424, 14.46262424)
    }

    Network.RetainPart = function(part)
        if typeof(part) == "Instance" and part:IsA("BasePart") and part:IsDescendantOf(Workspace) then
            table.insert(Network.BaseParts, part)
            part.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0, 0, 0)
            part.CanCollide = false
        end
    end

    local function EnablePartControl()
        LocalPlayer.ReplicationFocus = Workspace
        RunService.Heartbeat:Connect(function()
            sethiddenproperty(LocalPlayer, "SimulationRadius", math.huge)
            for _, part in pairs(Network.BaseParts) do
                if part:IsDescendantOf(Workspace) then
                    part.Velocity = Network.Velocity
                end
            end
        end)
    end

    EnablePartControl()
end

local function ForcePart(v)
    if v:IsA("Part") and not v.Anchored and not v.Parent:FindFirstChild("Humanoid") and not v.Parent:FindFirstChild("Head") and v.Name ~= "Handle" then
        for _, x in next, v:GetChildren() do
            if x:IsA("BodyAngularVelocity") or x:IsA("BodyForce") or x:IsA("BodyGyro") or x:IsA("BodyPosition") or x:IsA("BodyThrust") or x:IsA("BodyVelocity") or x:IsA("RocketPropulsion") then
                x:Destroy()
            end
        end
        if v:FindFirstChild("Attachment") then
            v:FindFirstChild("Attachment"):Destroy()
        end
        if v:FindFirstChild("AlignPosition") then
            v:FindFirstChild("AlignPosition"):Destroy()
        end
        if v:FindFirstChild("Torque") then
            v:FindFirstChild("Torque"):Destroy()
        end
        v.CanCollide = false
        
        local Torque = Instance.new("Torque", v)
        Torque.Torque = Vector3.new(1000000, 1000000, 1000000)
        local AlignPosition = Instance.new("AlignPosition", v)
        local Attachment2 = Instance.new("Attachment", v)
        Torque.Attachment0 = Attachment2
        AlignPosition.MaxForce = math.huge
        AlignPosition.MaxVelocity = math.huge
        AlignPosition.Responsiveness = 500
        AlignPosition.Attachment0 = Attachment2
        AlignPosition.Attachment1 = Attachment1
    end
end

local function toggleBlackHole()
    blackHoleActive = not blackHoleActive
    if blackHoleActive then
        for _, v in next, Workspace:GetDescendants() do
            ForcePart(v)
        end

        Workspace.DescendantAdded:Connect(function(v)
            if blackHoleActive then
                ForcePart(v)
            end
        end)

        spawn(function()
            while blackHoleActive and RunService.RenderStepped:Wait() do
                angle = angle + math.rad(2)

                local offsetX = math.cos(angle) * radius
                local offsetZ = math.sin(angle) * radius

                Attachment1.WorldCFrame = humanoidRootPart.CFrame * CFrame.new(offsetX, 0, offsetZ)
            end
        end)
    else
        Attachment1.WorldCFrame = CFrame.new(0, -1000, 0)
    end
end

LocalPlayer.CharacterAdded:Connect(function()
    humanoidRootPart, Attachment1 = setupPlayer()
    if blackHoleActive then
        toggleBlackHole()
    end
end)

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/miroeramaa/TurtleLib/main/TurtleUiLib.lua"))()
local window = library:Window("Projeto LKB")

window:Slider("Radius Blackhole",1,100,10, function(Value)
   radius = Value
end)

window:Toggle("Blackhole", true, function(Value)
       if Value then
            toggleBlackHole()
        else
            blackHoleActive = false
        end
end)

spawn(function()
    while true do
        RunService.RenderStepped:Wait()
        if blackHoleActive then
            angle = angle + math.rad(angleSpeed)
        end
    end
end)

toggleBlackHole()
    end
})

TrollTab:AddSection({ "Avatar RGB" })

local colors = { "Bright red", "Lime green", "Bright blue", "Bright yellow", "Bright cyan", "Hot pink", "Royal purple" }
local rgbEnabled = false

local function changeColor(color)
    local args = { color }
    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("ChangeBodyColor"):FireServer(unpack(args))
end

local function toggleRGBCharacter(enabled)
    rgbEnabled = enabled
    if rgbEnabled then
        while rgbEnabled do
            for _, color in ipairs(colors) do
                if not rgbEnabled then return end
                changeColor(color)
                wait(0.5)
            end
        end
    end
end

TrollTab:AddToggle({
    Name = "RGB Character",
    Description = "Deixa seu personagem RGB",
    Default = false,
    Callback = function(value)
        toggleRGBCharacter(value)
    end
})


TrollTab:AddSection({ "Cabelo RGB" })
local hairColors = {
    Color3.new(1, 1, 0), Color3.new(0, 0, 1), Color3.new(1, 0, 1), Color3.new(1, 1, 1),
    Color3.new(0, 1, 0), Color3.new(0.5, 0, 1), Color3.new(1, 0.647, 0), Color3.new(0, 1, 1)
}
local isActive = false


local function changeHairColor()
    local i = 1
    while isActive do
        if not isActive then break end
        local args = { [1] = "ChangeHairColor2", [2] = hairColors[i] }
        game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Max1y"):FireServer(unpack(args))
        wait(0.1)
        i = i % #hairColors + 1
    end
end


TrollTab:AddToggle({
    Name = "Cabelo RGB",
    Description = "Deixa Seu Cabelo RGB",
    Default = false,
    Callback = function(value)
        isActive = value
        if isActive then
            changeHairColor()
        end
    end
})


-- Tab 4: Anti Sit
TrollTab:AddSection({ "Anti Sit" })
TrollTab:AddToggle({
    Name = "Anti Sit",
    Description = "Não Deixa seu personagem Sentar",
    Default = false,
    Callback = function(Value)
        local player = game.Players.LocalPlayer
        local connections = {}
        local runService = game:GetService("RunService")


        local function preventSitting(humanoid)
            if humanoid then
                humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
                local sitConnection = humanoid.StateChanged:Connect(function(_, newState)
                    if newState == Enum.HumanoidStateType.Seated then
                        humanoid:ChangeState(Enum.HumanoidStateType.GettingUp)
                    end
                end)
                table.insert(connections, sitConnection)
            end
        end


        local function monitorCharacter()
            local function onCharacterAdded(character)
                local humanoid = character:WaitForChild("Humanoid")
                preventSitting(humanoid)
            end


            local characterAddedConnection = player.CharacterAdded:Connect(onCharacterAdded)
            table.insert(connections, characterAddedConnection)


            if player.Character then
                onCharacterAdded(player.Character)
            end
        end


        local function resetSitting()
            for _, connection in ipairs(connections) do
                connection:Disconnect()
            end
            connections = {}
            local humanoid = player.Character and player.Character:FindFirstChildOfClass("Humanoid")
            if humanoid then
                humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
            end
        end


        if Value then
            monitorCharacter()
            local heartbeatConnection = runService.Heartbeat:Connect(function()
                local humanoid = player.Character and player.Character:FindFirstChildOfClass("Humanoid")
                if humanoid then
                    humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
                end
            end)
            table.insert(connections, heartbeatConnection)
        else
            resetSitting()
        end
    end
})
TrollTab:AddSection({ "Naruto" })

shinraSound = nil
cancelShinra = false

TrollTab:AddButton({
    Name = "[OP] Shinra Tensei - Pain",
    Callback = function()
local TextChatService = game:GetService("TextChatService")
local Lighting = game:GetService("Lighting")
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Player = Players.LocalPlayer

cancelShinra = false

if TextChatService.ChatVersion == Enum.ChatVersion.TextChatService then 
    TextChatService.TextChannels.RBXGeneral:SendAsync(
        "hi\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\rShinra Tensei..."
    )
else 
end

task.spawn(function()
local player = game.Players.LocalPlayer
    if not player.Character or not player.Character:FindFirstChild("HumanoidRootPart") then return end
    local root = player.Character.HumanoidRootPart

    local bodyPos = Instance.new("BodyPosition")
    bodyPos.MaxForce = Vector3.new(1e5, 1e5, 1e5)
    bodyPos.Position = root.Position
    bodyPos.Parent = root

    local targetUp = root.Position + Vector3.new(0, 10, 0)
    for i = 1, 10 do
        bodyPos.Position = bodyPos.Position:Lerp(targetUp, 0.1)
        task.wait(0.03)
    end

    task.wait(2)

    for i = 1, 10 do
        bodyPos.Position = bodyPos.Position:Lerp(root.Position, 0.1)
        task.wait(0.03)
    end
    
    bodyPos:Destroy()
end)

local RE = ReplicatedStorage:WaitForChild("RE")
local ClearEvent = RE:FindFirstChild("1Clea1rTool1s")
local ToolEvent = RE:FindFirstChild("1Too1l")
local FireEvent = RE:FindFirstChild("1Gu1n")

local function clearAllTools()
    if ClearEvent then
        ClearEvent:FireServer("ClearAllTools")
    end
end

local function getAssault()
    if ToolEvent then
        ToolEvent:InvokeServer("PickingTools", "Assault")
    end
end

local function hasAssault()
    return Player.Backpack:FindFirstChild("Assault") ~= nil
end

local function fireAtPart(targetPart)
    local gunScript = Player.Backpack:FindFirstChild("Assault")
        and Player.Backpack.Assault:FindFirstChild("GunScript_Local")

    if not gunScript or not targetPart then return end

    local args = {
        targetPart,
        targetPart,
        Vector3.new(1e14, 1e14, 1e14),
        targetPart.Position,
        gunScript:FindFirstChild("MuzzleEffect"),
        gunScript:FindFirstChild("HitEffect"),
        0,
        0,
        { false },
        {
            25,
            Vector3.new(100, 100, 100),
            BrickColor.new(29),
            0.25,
            Enum.Material.SmoothPlastic,
            0.25
        },
        true,
        false
    }

    FireEvent:FireServer(unpack(args))
end

local function fireAtAllPlayers(times)
    for i = 1, times do
        if cancelShinra then break end
        for _, player in ipairs(Players:GetPlayers()) do
            if player ~= Player and player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                fireAtPart(player.Character.HumanoidRootPart)
                task.wait(0.1)
            end
        end
    end
end

local selectedAudioID = 127171723747143

task.spawn(function()
local remote = ReplicatedStorage:FindFirstChild("RE") and ReplicatedStorage.RE:FindFirstChild("1Gu1nSound1s")
if remote then
remote:FireServer(workspace, selectedAudioID, 1)
end

local root = Player.Character and Player.Character:FindFirstChild("HumanoidRootPart")
if root then
local sound = Instance.new("Sound")
sound.SoundId = "rbxassetid://" .. selectedAudioID
sound.Volume = 1
sound.Looped = false
sound.Parent = root
sound:Play()
sound.Ended:Connect(function() sound:Destroy() end)
else
end
end)
            
task.spawn(function()
    while not cancelShinra do
        clearAllTools()
        getAssault()

        repeat
            task.wait(0.2)
        until hasAssault() or cancelShinra

        if not cancelShinra then
            fireAtAllPlayers(3)
            task.wait(1)
        end
    end
end)
end
})

TrollTab:AddButton({
    Name = "Cancel Shinra Tensei",
    Callback = function()
        cancelShinra = true
    
    if shinraSound then
            shinraSound:Stop()
            shinraSound:Destroy()
            shinraSound = nil
        end
    end
})

TrollTab:AddSection({ "Jujutsu Kaisen" })

cancelExpansion = false
expansionSound = nil
expansionModel = nil
originalSky = nil

TrollTab:AddButton({
    Name = "[OP] Domain Expansion - Gojo",
    Callback = function()
local TextChatService = game:GetService("TextChatService")
local Lighting = game:GetService("Lighting")
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Player = Players.LocalPlayer

cancelExpansion = false

if TextChatService.ChatVersion == Enum.ChatVersion.TextChatService then 
    TextChatService.TextChannels.RBXGeneral:SendAsync(
        "hi\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\rDomain Expansion..."
    )
else 
end

local function ativarDominio()
    local char = Player.Character or Player.CharacterAdded:Wait()
    local hrp = char:WaitForChild("HumanoidRootPart")

    local dominio = Instance.new("Model", workspace)
    dominio.Name = "InfiniteVoid"
    expansionModel = dominio

    local esfera = Instance.new("Part")
    esfera.Shape = Enum.PartType.Ball
    esfera.Size = Vector3.new(300, 300, 300)
    esfera.Position = hrp.Position
    esfera.Anchored = true
    esfera.CanCollide = false
    esfera.Material = Enum.Material.ForceField
    esfera.Transparency = 0.3
    esfera.Color = Color3.fromRGB(0, 0, 0)
    esfera.Parent = dominio

    local luz = Instance.new("PointLight", esfera)
    luz.Color = Color3.fromRGB(0, 153, 255)
    luz.Brightness = 10
    luz.Range = 300

    local ps = Instance.new("ParticleEmitter", esfera)
    ps.Texture = "rbxassetid://243660364"
    ps.Color = ColorSequence.new(Color3.fromRGB(0, 153, 255))
    ps.LightEmission = 1
    ps.Size = NumberSequence.new(3)
    ps.Transparency = NumberSequence.new(0.2)
    ps.Rate = 1000
    ps.Lifetime = NumberRange.new(2)
    ps.Speed = NumberRange.new(0)
    ps.VelocitySpread = 180

    local som = Instance.new("Sound", esfera)
    som.SoundId = "rbxassetid://1843527678"
    som.Volume = 2
    som.Looped = true
    som:Play()
    expansionSound = som

    originalSky = Lighting:FindFirstChildOfClass("Sky")
    if originalSky then
        originalSky.Parent = nil
    end

    local newSky = Instance.new("Sky", Lighting)
    newSky.SkyboxBk = "rbxassetid://159454299"
    newSky.SkyboxDn = "rbxassetid://159454296"
    newSky.SkyboxFt = "rbxassetid://159454293"
    newSky.SkyboxLf = "rbxassetid://159454286"
    newSky.SkyboxRt = "rbxassetid://159454300"
    newSky.SkyboxUp = "rbxassetid://159454288"
end

ativarDominio()

local selectedAudioID = 140031333626044

task.spawn(function()
    while not cancelExpansion do
        local remote = ReplicatedStorage:FindFirstChild("RE") and ReplicatedStorage.RE:FindFirstChild("1Gu1nSound1s")
        if remote then
            remote:FireServer(workspace, selectedAudioID, 1)
        end

        local root = Player.Character and Player.Character:FindFirstChild("HumanoidRootPart")
        if root then
            local sound = Instance.new("Sound")
            sound.SoundId = "rbxassetid://" .. selectedAudioID
            sound.Volume = 1
            sound.Looped = false
            sound.Parent = root
            sound:Play()
            sound.Ended:Connect(function() sound:Destroy() end)
            task.wait(sound.TimeLength + 0.1)
        else
            break
        end
    end
end)

local RE = ReplicatedStorage:WaitForChild("RE")
local ClearEvent = RE:FindFirstChild("1Clea1rTool1s")
local ToolEvent = RE:FindFirstChild("1Too1l")
local FireEvent = RE:FindFirstChild("1Gu1n")

local function clearAllTools()
    if ClearEvent then
        ClearEvent:FireServer("ClearAllTools")
    end
end

local function getAssault()
    if ToolEvent then
        ToolEvent:InvokeServer("PickingTools", "Assault")
    end
end

local function hasAssault()
    return Player.Backpack:FindFirstChild("Assault") ~= nil
end

local function fireAtPart(targetPart)
    local gunScript = Player.Backpack:FindFirstChild("Assault")
        and Player.Backpack.Assault:FindFirstChild("GunScript_Local")

    if not gunScript or not targetPart then return end

    local args = {
        targetPart,
        targetPart,
        Vector3.new(1e14, 1e14, 1e14),
        targetPart.Position,
        gunScript:FindFirstChild("MuzzleEffect"),
        gunScript:FindFirstChild("HitEffect"),
        0,
        0,
        { false },
        {
            25,
            Vector3.new(100, 100, 100),
            BrickColor.new(29),
            0.25,
            Enum.Material.SmoothPlastic,
            0.25
        },
        true,
        false
    }

    FireEvent:FireServer(unpack(args))
end

local function fireAtAllPlayers(times)
    for i = 1, times do
        if cancelExpansion then break end
        for _, player in ipairs(Players:GetPlayers()) do
            if player ~= Player and player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                fireAtPart(player.Character.HumanoidRootPart)
                task.wait(0.1)
            end
        end
    end
end

task.spawn(function()
    while not cancelExpansion do
        clearAllTools()
        getAssault()

        repeat
            task.wait(0.2)
        until hasAssault() or cancelExpansion

        if not cancelExpansion then
            fireAtAllPlayers(3)
            task.wait(1)
        end
    end
end)
end
})

TrollTab:AddButton({
    Name = "Cancel Domain Expansion",
    Callback = function()
        cancelExpansion = true

        if expansionSound then
            expansionSound:Stop()
            expansionSound:Destroy()
            expansionSound = nil
        end

        if expansionModel and expansionModel.Parent then
            expansionModel:Destroy()
            expansionModel = nil
        end

        local Lighting = game:GetService("Lighting")
        local currentSky = Lighting:FindFirstChildOfClass("Sky")
        if currentSky then currentSky:Destroy() end

        if originalSky then
            originalSky.Parent = Lighting
            originalSky = nil
        end
    end
})
TrollTab:AddSection({ "Natural Disasters" })
TrollTab:AddButton({
    Name = "[OP] Tornado - Pirate Ship (Large)",
    Callback = function()
local RS = game:GetService("ReplicatedStorage")
local RunService = game:GetService("RunService")
local TextChatService = game:GetService("TextChatService")
local Player = game.Players.LocalPlayer
local Character = Player.Character or Player.CharacterAdded:Wait()
local Humanoid = Character:WaitForChild("Humanoid")
local RootPart = Character:WaitForChild("HumanoidRootPart")
local Vehicles = workspace:WaitForChild("Vehicles")

if TextChatService.ChatVersion == Enum.ChatVersion.TextChatService then 
    TextChatService.TextChannels.RBXGeneral:SendAsync(
        "hi\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\rTornado has appeared! Be careful..."
    )
else 
end

local selectedAudioID = 9068077052
local function playAudio()
    if not selectedAudioID then
        return
    end

    local args = {
        [1] = workspace,
        [2] = selectedAudioID,
        [3] = 1,
    }

    for i = 1, 5 do
        RS.RE:FindFirstChild("1Gu1nSound1s"):FireServer(unpack(args))

        local sound = Instance.new("Sound")
        sound.SoundId = "rbxassetid://" .. tostring(selectedAudioID)
        sound.Parent = Player.Character and Player.Character:FindFirstChild("HumanoidRootPart")
        if sound.Parent then
            sound:Play()
        else
            break
        end

        task.wait(1.5)
        sound:Destroy()
    end
end

local function spawnBoat()
    RootPart.CFrame = CFrame.new(1754, -2, 58)
    task.wait(0.5)
    RS:WaitForChild("RE"):FindFirstChild("1Ca1r"):FireServer("PickingBoat", "PirateFree")
    task.wait(1)
    return Vehicles:FindFirstChild(Player.Name .. "Car")
end

local PCar = spawnBoat()
if not PCar then
    return
end

local Seat = PCar:FindFirstChild("Body") and PCar.Body:FindFirstChild("VehicleSeat")
if not Seat then
    return
end

repeat
    task.wait(0.1)
    RootPart.CFrame = Seat.CFrame * CFrame.new(0, 1, 0)
until Humanoid.SeatPart == Seat

task.spawn(playAudio)

task.delay(4, function()
    if Humanoid.SeatPart then
        Humanoid.Sit = false
    end
    RootPart.CFrame = CFrame.new(0, 0, 0)
end)

local RE_Flip = RS:WaitForChild("RE"):WaitForChild("1Player1sCa1r")
task.spawn(function()
    while PCar and PCar.Parent do
        RE_Flip:FireServer("Flip")
        task.wait(0.5)
    end
end)

local waypoints = {
    Vector3.new(-16, 0, -47),
    Vector3.new(-110, 0, -45),
    Vector3.new(16, 0, -55)
}

local currentIndex = 1
local nextIndex = 2
local moveSpeed = 15
local rotationSpeed = math.rad(720)
local progress = 0
local currentRotation = 0

local function lerpCFrame(a, b, t)
    return a:lerp(b, t)
end

RunService.Heartbeat:Connect(function(dt)
    if not (PCar and PCar.PrimaryPart) then return end

    local startPos = waypoints[currentIndex]
    local endPos = waypoints[nextIndex]

    progress += (moveSpeed * dt) / (startPos - endPos).Magnitude
    if progress >= 1 then
        progress = 0
        currentIndex = nextIndex
        nextIndex = (nextIndex % #waypoints) + 1
    end

    local newPos = lerpCFrame(CFrame.new(startPos), CFrame.new(endPos), progress).p
    currentRotation += rotationSpeed * dt

    local cf = CFrame.new(newPos) * CFrame.Angles(0, currentRotation, 0)
    PCar:SetPrimaryPartCFrame(cf)
end)
end
})

TrollTab:AddButton({
    Name = "Cancel Tornado",
    Callback = function()
        local success, err = pcall(function()
            local args = { "DeleteAllVehicles" }
            game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Ca1r"):FireServer(unpack(args))
        end)

        if not success then
        else
        end
    end
})

local Troll = Window:MakeTab({ Title = "Trolling Jogadores", Icon = "rbxassetid://131153193945220" })


local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local VirtualInputManager = game:GetService("VirtualInputManager")
local RunService = game:GetService("RunService")
local cam = workspace.CurrentCamera


local selectedPlayerName = nil
local methodKill = nil
getgenv().Target = nil
local Character = LocalPlayer.Character
local Humanoid = Character and Character:WaitForChild("Humanoid")
local RootPart = Character and Character:WaitForChild("HumanoidRootPart")

-- Função para limpar o sofá (couch)
local function cleanupCouch()
    local char = LocalPlayer.Character
    if char then
        local couch = char:FindFirstChild("Chaos.Couch") or LocalPlayer.Backpack:FindFirstChild("Chaos.Couch")
        if couch then
            couch:Destroy()
        end
    end
    -- Limpar ferramentas via remoto
    ReplicatedStorage:WaitForChild("RE"):WaitForChild("1Clea1rTool1s"):FireServer("ClearAllTools")
end

-- Conectar evento CharacterAdded
LocalPlayer.CharacterAdded:Connect(function(newCharacter)
    Character = newCharacter
    Humanoid = newCharacter:WaitForChild("Humanoid")
    RootPart = newCharacter:WaitForChild("HumanoidRootPart")
    cleanupCouch()
    
    -- Conectar evento Died para o novo Humanoid
    Humanoid.Died:Connect(function()
        cleanupCouch()
    end)
end)

-- Conectar evento Died para o Humanoid inicial, se existir
if Humanoid then
    Humanoid.Died:Connect(function()
        cleanupCouch()
    end)
end

-- Função KillPlayerCouch
local function KillPlayerCouch()
    if not selectedPlayerName then
        warn("Erro: Nenhum jogador selecionado")
        return
    end
    local target = Players:FindFirstChild(selectedPlayerName)
    if not target or not target.Character then
        warn("Erro: Jogador alvo não encontrado ou sem personagem")
        return
    end

    local char = LocalPlayer.Character
    if not char then
        warn("Erro: Personagem do jogador local não encontrado")
        return
    end
    local hum = char:FindFirstChildOfClass("Humanoid")
    local root = char:FindFirstChild("HumanoidRootPart")
    local tRoot = target.Character and target.Character:FindFirstChild("HumanoidRootPart")
    if not hum or not root or not tRoot then
        warn("Erro: Componentes necessários não encontrados")
        return
    end

    local originalPos = root.Position 
    local sitPos = Vector3.new(145.51, -350.09, 21.58)

    ReplicatedStorage:WaitForChild("RE"):WaitForChild("1Clea1rTool1s"):FireServer("ClearAllTools")
    task.wait(0.2)

    ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer("PickingTools", "Couch")
    task.wait(0.3)

    local tool = LocalPlayer.Backpack:FindFirstChild("Couch")
    if tool then tool.Parent = char end
    task.wait(0.1)

    VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.F, false, game)
    task.wait(0.1)

    hum:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
    hum.PlatformStand = false
    cam.CameraSubject = target.Character:FindFirstChild("Head") or tRoot or hum

    local align = Instance.new("BodyPosition")
    align.Name = "BringPosition"
    align.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
    align.D = 10
    align.P = 30000
    align.Position = root.Position
    align.Parent = tRoot

    task.spawn(function()
        local angle = 0
        local startTime = tick()
        while tick() - startTime < 5 and target and target.Character and target.Character:FindFirstChildOfClass("Humanoid") do
            local tHum = target.Character:FindFirstChildOfClass("Humanoid")
            if not tHum or tHum.Sit then break end

            local hrp = target.Character.HumanoidRootPart
            local adjustedPos = hrp.Position + (hrp.Velocity / 1.5)

            angle += 50
            root.CFrame = CFrame.new(adjustedPos + Vector3.new(0, 2, 0)) * CFrame.Angles(math.rad(angle), 0, 0)
            align.Position = root.Position + Vector3.new(2, 0, 0)

            task.wait()
        end

        align:Destroy()
        hum:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
        hum.PlatformStand = false
        cam.CameraSubject = hum

        for _, p in pairs(char:GetDescendants()) do
            if p:IsA("BasePart") then
                p.Velocity = Vector3.zero
                p.RotVelocity = Vector3.zero
            end
        end

        task.wait(0.1)
        root.CFrame = CFrame.new(sitPos)
        task.wait(0.3)

        local tool = char:FindFirstChild("Couch")
        if tool then tool.Parent = LocalPlayer.Backpack end

        task.wait(0.01)
        ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer("PickingTools", "Couch")
        task.wait(0.2)
        root.CFrame = CFrame.new(originalPos)
    end)
end

-- Função BringPlayerLLL
local function BringPlayerLLL()
    if not selectedPlayerName then
        warn("Erro: Nenhum jogador selecionado")
        return
    end
    local target = Players:FindFirstChild(selectedPlayerName)
    if not target or not target.Character then
        warn("Erro: Jogador alvo não encontrado ou sem personagem")
        return
    end

    local char = LocalPlayer.Character
    if not char then
        warn("Erro: Personagem do jogador local não encontrado")
        return
    end
    local hum = char:FindFirstChildOfClass("Humanoid")
    local root = char:FindFirstChild("HumanoidRootPart")
    local tRoot = target.Character and target.Character:FindFirstChild("HumanoidRootPart")
    if not hum or not root or not tRoot then
        warn("Erro: Componentes necessários não encontrados")
        return
    end

    local originalPos = root.Position 
    ReplicatedStorage:WaitForChild("RE"):WaitForChild("1Clea1rTool1s"):FireServer("ClearAllTools")
    task.wait(0.2)

    ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer("PickingTools", "Couch")
    task.wait(0.3)

    local tool = LocalPlayer.Backpack:FindFirstChild("Couch")
    if tool then
        tool.Parent = char
    end
    task.wait(0.1)

    VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.F, false, game)
    task.wait(0.1)

    hum:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
    hum.PlatformStand = false
    cam.CameraSubject = target.Character:FindFirstChild("Head") or tRoot or hum

    local align = Instance.new("BodyPosition")
    align.Name = "BringPosition"
    align.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
    align.D = 10
    align.P = 30000
    align.Position = root.Position
    align.Parent = tRoot

    task.spawn(function()
        local angle = 0
        local startTime = tick()
        while tick() - startTime < 5 and target and target.Character and target.Character:FindFirstChildOfClass("Humanoid") do
            local tHum = target.Character:FindFirstChildOfClass("Humanoid")
            if not tHum or tHum.Sit then break end

            local hrp = target.Character.HumanoidRootPart
            local adjustedPos = hrp.Position + (hrp.Velocity / 1.5)

            angle += 50
            root.CFrame = CFrame.new(adjustedPos + Vector3.new(0, 2, 0)) * CFrame.Angles(math.rad(angle), 0, 0)
            align.Position = root.Position + Vector3.new(2, 0, 0)

            task.wait()
        end

        align:Destroy()
        hum:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
        hum.PlatformStand = false
        cam.CameraSubject = hum

        for _, p in pairs(char:GetDescendants()) do
            if p:IsA("BasePart") then
                p.Velocity = Vector3.zero
                p.RotVelocity = Vector3.zero
            end
        end

        task.wait(0.1)
        root.Anchored = true
        root.CFrame = CFrame.new(originalPos)
        task.wait(0.001)
        root.Anchored = false

        task.wait(0.7)
        local tool = char:FindFirstChild("Couch")
        if tool then
            tool.Parent = LocalPlayer.Backpack
        end

        task.wait(0.001)
        ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer("PickingTools", "Couch")
    end)
end

-- Função BringWithCouch
local function BringWithCouch()
    local targetPlayer = Players:FindFirstChild(getgenv().Target)
    if not targetPlayer then
        warn("Erro: Nenhum jogador alvo selecionado")
        return
    end
    if not targetPlayer.Character or not targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
        warn("Erro: Jogador alvo sem personagem ou HumanoidRootPart")
        return
    end

    local args = { [1] = "ClearAllTools" }
    ReplicatedStorage.RE["1Clea1rTool1s"]:FireServer(unpack(args))
    local args = { [1] = "PickingTools", [2] = "Couch" }
    ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))

    local couch = LocalPlayer.Backpack:WaitForChild("Couch", 2)
    if not couch then
        warn("Erro: Sofá não encontrado no Backpack")
        return
    end

    couch.Name = "Chaos.Couch"
    local seat1 = couch:FindFirstChild("Seat1")
    local seat2 = couch:FindFirstChild("Seat2")
    local handle = couch:FindFirstChild("Handle")
    if seat1 and seat2 and handle then
        seat1.Disabled = true
        seat2.Disabled = true
        handle.Name = "Handle "
    else
        warn("Erro: Componentes do sofá não encontrados")
        return
    end
    couch.Parent = LocalPlayer.Character

    local tet = Instance.new("BodyVelocity", seat1)
    tet.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
    tet.P = 1250
    tet.Velocity = Vector3.new(0, 0, 0)
    tet.Name = "#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W"

    repeat
        for m = 1, 35 do
            local pos = { x = 0, y = 0, z = 0 }
            local tRoot = targetPlayer.Character and targetPlayer.Character.HumanoidRootPart
            if not tRoot then break end
            pos.x = tRoot.Position.X + (tRoot.Velocity.X / 2)
            pos.y = tRoot.Position.Y + (tRoot.Velocity.Y / 2)
            pos.z = tRoot.Position.Z + (tRoot.Velocity.Z / 2)
            seat1.CFrame = CFrame.new(Vector3.new(pos.x, pos.y, pos.z)) * CFrame.new(-2, 2, 0)
            task.wait()
        end
        tet:Destroy()
        couch.Parent = LocalPlayer.Backpack
        task.wait()
        couch:FindFirstChild("Handle ").Name = "Handle"
        task.wait(0.2)
        couch.Parent = LocalPlayer.Character
        task.wait()
        couch.Parent = LocalPlayer.Backpack
        couch.Handle.Name = "Handle "
        task.wait(0.2)
        couch.Parent = LocalPlayer.Character
        tet = Instance.new("BodyVelocity", seat1)
        tet.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
        tet.P = 1250
        tet.Velocity = Vector3.new(0, 0, 0)
        tet.Name = "#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W"
    until targetPlayer.Character and targetPlayer.Character.Humanoid and targetPlayer.Character.Humanoid.Sit == true
    task.wait()
    tet:Destroy()
    couch.Parent = LocalPlayer.Backpack
    task.wait()
    couch:FindFirstChild("Handle ").Name = "Handle"
    task.wait(0.3)
    couch.Parent = LocalPlayer.Character
    task.wait(0.3)
    couch.Grip = CFrame.new(Vector3.new(0, 0, 0))
    task.wait(0.3)
    ReplicatedStorage.RE["1Clea1rTool1s"]:FireServer("ClearAllTools")
end

-- Função KillWithCouch
local function KillWithCouch()
    local targetPlayer = Players:FindFirstChild(getgenv().Target)
    if not targetPlayer then
        warn("Erro: Nenhum jogador alvo selecionado")
        return
    end
    if not targetPlayer.Character or not targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
        warn("Erro: Jogador alvo sem personagem ou HumanoidRootPart")
        return
    end

    local args = { [1] = "ClearAllTools" }
    ReplicatedStorage.RE["1Clea1rTool1s"]:FireServer(unpack(args))
    local args = { [1] = "PickingTools", [2] = "Couch" }
    ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))

    local couch = LocalPlayer.Backpack:WaitForChild("Couch", 2)
    if not couch then
        warn("Erro: Sofá não encontrado no Backpack")
        return
    end

    couch.Name = "Chaos.Couch"
    local seat1 = couch:FindFirstChild("Seat1")
    local seat2 = couch:FindFirstChild("Seat2")
    local handle = couch:FindFirstChild("Handle")
    if seat1 and seat2 and handle then
        seat1.Disabled = true
        seat2.Disabled = true
        handle.Name = "Handle "
    else
        warn("Erro: Componentes do sofá não encontrados")
        return
    end
    couch.Parent = LocalPlayer.Character

    local tet = Instance.new("BodyVelocity", seat1)
    tet.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
    tet.P = 1250
    tet.Velocity = Vector3.new(0, 0, 0)
    tet.Name = "#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W"

    repeat
        for m = 1, 35 do
            local pos = { x = 0, y = 0, z = 0 }
            local tRoot = targetPlayer.Character and targetPlayer.Character.HumanoidRootPart
            if not tRoot then break end
            pos.x = tRoot.Position.X + (tRoot.Velocity.X / 2)
            pos.y = tRoot.Position.Y + (tRoot.Velocity.Y / 2)
            pos.z = tRoot.Position.Z + (tRoot.Velocity.Z / 2)
            seat1.CFrame = CFrame.new(Vector3.new(pos.x, pos.y, pos.z)) * CFrame.new(-2, 2, 0)
            task.wait()
        end
        tet:Destroy()
        couch.Parent = LocalPlayer.Backpack
        task.wait()
        couch:FindFirstChild("Handle ").Name = "Handle"
        task.wait(0.2)
        couch.Parent = LocalPlayer.Character
        task.wait()
        couch.Parent = LocalPlayer.Backpack
        couch.Handle.Name = "Handle "
        task.wait(0.2)
        couch.Parent = LocalPlayer.Character
        tet = Instance.new("BodyVelocity", seat1)
        tet.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
        tet.P = 1250
        tet.Velocity = Vector3.new(0, 0, 0)
        tet.Name = "#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W"
    until targetPlayer.Character and targetPlayer.Character.Humanoid and targetPlayer.Character.Humanoid.Sit == true
    task.wait()
    couch.Parent = LocalPlayer.Backpack
    seat1.CFrame = CFrame.new(Vector3.new(9999, -450, 9999))
    seat2.CFrame = CFrame.new(Vector3.new(9999, -450, 9999))
    couch.Parent = LocalPlayer.Character
    task.wait(0.1)
    couch.Parent = LocalPlayer.Backpack
    task.wait(2)
    local bv = seat1:FindFirstChild("#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W")
    if bv then bv:Destroy() end
    ReplicatedStorage.RE["1Clea1rTool1s"]:FireServer("ClearAllTools")
end
local function FlingBall(target)

    local players = game:GetService("Players")
    local player = players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local humanoid = character:WaitForChild("Humanoid")
    local hrp = character:WaitForChild("HumanoidRootPart")
    local backpack = player:WaitForChild("Backpack")
    local ServerBalls = workspace.WorkspaceCom:WaitForChild("001_SoccerBalls")

    local function GetBall()
        if not backpack:FindFirstChild("SoccerBall") then
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer("PickingTools", "SoccerBall")
        end
        repeat task.wait() until backpack:FindFirstChild("SoccerBall")
        backpack.SoccerBall.Parent = character
        repeat task.wait() until ServerBalls:FindFirstChild("Soccer" .. player.Name)
        character.SoccerBall.Parent = backpack
        return ServerBalls:FindFirstChild("Soccer" .. player.Name)
    end

    local Ball = ServerBalls:FindFirstChild("Soccer" .. player.Name) or GetBall()
    Ball.CanCollide = false
    Ball.Massless = true
    Ball.CustomPhysicalProperties = PhysicalProperties.new(0.0001, 0, 0)

    if target ~= player then
        local tchar = target.Character
        if tchar and tchar:FindFirstChild("HumanoidRootPart") and tchar:FindFirstChild("Humanoid") then
            local troot = tchar.HumanoidRootPart
            local thum = tchar.Humanoid

            if Ball:FindFirstChildWhichIsA("BodyVelocity") then
                Ball:FindFirstChildWhichIsA("BodyVelocity"):Destroy()
            end

            local bv = Instance.new("BodyVelocity")
            bv.Name = "FlingPower"
            bv.Velocity = Vector3.new(9e8, 9e8, 9e8)
            bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bv.P = 9e900
            bv.Parent = Ball

            workspace.CurrentCamera.CameraSubject = thum
            local StartTime = os.time()
            repeat
                if troot.Velocity.Magnitude > 0 then
                -- Cálculo da posição ajustada com base na velocidade do alvo
                local pos_x = troot.Position.X + (troot.Velocity.X / 1.5)
                local pos_y = troot.Position.Y + (troot.Velocity.Y / 1.5)
                local pos_z = troot.Position.Z + (troot.Velocity.Z / 1.5)

                -- Posiciona a bola diretamente na posição ajustada
                local position = Vector3.new(pos_x, pos_y, pos_z)
                Ball.CFrame = CFrame.new(position)
                Ball.Orientation += Vector3.new(45, 60, 30)
else
for i, v in pairs(tchar:GetChildren()) do
if v:IsA("BasePart") and v.CanCollide and not v.Anchored then
Ball.CFrame = v.CFrame
task.wait(1/6000)
end
end
end
                task.wait(1/6000)
            until troot.Velocity.Magnitude > 1000 or thum.Health <= 0 or not tchar:IsDescendantOf(workspace) or target.Parent ~= players
            workspace.CurrentCamera.CameraSubject = humanoid
        end
    end
end


local function playerCorrupt()
    local targetPlayer = Players:FindFirstChild(getgenv().Target)
    if not targetPlayer then
        return
    end
    if not targetPlayer.Character or not targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
        return
    end

    local args = { [1] = "ClearAllTools" }
    ReplicatedStorage.RE["1Clea1rTool1s"]:FireServer(unpack(args))
    local args = { [1] = "PickingTools", [2] = "Couch" }
    ReplicatedStorage.RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))

    local couch = LocalPlayer.Backpack:WaitForChild("Couch", 2)
    if not couch then
        return
    end

    couch.Name = "Chaos.Couch"
    local seat1 = couch:FindFirstChild("Seat1")
    local seat2 = couch:FindFirstChild("Seat2")
    local handle = couch:FindFirstChild("Handle")
    if seat1 and seat2 and handle then
        seat1.Disabled = true
        seat2.Disabled = true
        handle.Name = "Handle "
    else
        return
    end
    couch.Parent = LocalPlayer.Character

    local tet = Instance.new("BodyVelocity", seat1)
    tet.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
    tet.P = 1250
    tet.Velocity = Vector3.new(0, 0, 0)
    tet.Name = "#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W"

    repeat
        for m = 1, 35 do
            local pos = { x = 0, y = 0, z = 0 }
            local tRoot = targetPlayer.Character and targetPlayer.Character.HumanoidRootPart
            if not tRoot then break end
            pos.x = tRoot.Position.X + (tRoot.Velocity.X / 2)
            pos.y = tRoot.Position.Y + (tRoot.Velocity.Y / 2)
            pos.z = tRoot.Position.Z + (tRoot.Velocity.Z / 2)
            seat1.CFrame = CFrame.new(Vector3.new(pos.x, pos.y, pos.z)) * CFrame.new(-2, 2, 0)
            task.wait()
        end
        tet:Destroy()
        couch.Parent = LocalPlayer.Backpack
        task.wait()
        couch:FindFirstChild("Handle ").Name = "Handle"
        task.wait(0.2)
        couch.Parent = LocalPlayer.Character
        task.wait()
        couch.Parent = LocalPlayer.Backpack
        couch.Handle.Name = "Handle "
        task.wait(0.2)
        couch.Parent = LocalPlayer.Character
        tet = Instance.new("BodyVelocity", seat1)
        tet.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
        tet.P = 1250
        tet.Velocity = Vector3.new(0, 0, 0)
        tet.Name = "#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W"
    until targetPlayer.Character and targetPlayer.Character.Humanoid and targetPlayer.Character.Humanoid.Sit == true
    task.wait()
    couch.Parent = LocalPlayer.Backpack
    seat1.CFrame = CFrame.new(Vector3.new(9e10, 9e10, 9e10))
    seat2.CFrame.new(Vector3.new(9e10, 9e10, 9e10))
    couch.Parent = LocalPlayer.Character
    task.wait(0.1)
    couch.Parent = LocalPlayer.Backpack
    task.wait(2)
    local bv = seat1:FindFirstChild("#mOVOOEPF$#@F$#GERE..>V<<<<EW<V<<W")
    if bv then bv:Destroy() end
    ReplicatedStorage.RE["1Clea1rTool1s"]:FireServer("ClearAllTools")
end

    local PlayerSection = Troll:AddSection({ Name = "Troll Player" })

    -- Função para obter lista de jogadores
    local function getPlayerList()
        local players = Players:GetPlayers()
        local playerNames = {}
        for _, player in ipairs(players) do
            if player ~= LocalPlayer then
                table.insert(playerNames, player.Name)
            end
        end
        return playerNames
    end

    local killDropdown = Troll:AddDropdown({
        Name = "Selecionar Jogador",
        Options = getPlayerList(),
        Default = "",
        Callback = function(value)
            selectedPlayerName = value
            getgenv().Target = value
            print("Jogador selecionado: " .. tostring(value))
        end
    })

    Troll:AddButton({
        Name = "Atualizar Player List",
        Callback = function()
            local tablePlayers = Players:GetPlayers()
            local newPlayers = {}
            if killDropdown and #tablePlayers > 0 then
                for _, player in ipairs(tablePlayers) do
                    if player.Name ~= LocalPlayer.Name then
                        table.insert(newPlayers, player.Name)
                    end
                end
                killDropdown:Set(newPlayers)
                print("Lista de jogadores atualizada: ", table.concat(newPlayers, ", "))
                if selectedPlayerName and not Players:FindFirstChild(selectedPlayerName) then
                    selectedPlayerName = nil
                    getgenv().Target = nil
                    killDropdown:SetValue("")
                    print("Seleção resetada, jogador não está mais no servidor.")
                end
            else
                print("Erro: Dropdown não encontrado ou nenhum jogador disponível.")
            end
        end
    })

    Troll:AddButton({
        Name = "Teleportar até o Player",
        Callback = function()
            if not selectedPlayerName or not Players:FindFirstChild(selectedPlayerName) then
                print("Erro: Player não selecionado ou não existe")
                return
            end
            local character = LocalPlayer.Character
            local humanoidRootPart = character and character:FindFirstChild("HumanoidRootPart")
            if not humanoidRootPart then
                warn("Erro: HumanoidRootPart do jogador local não encontrado")
                return
            end

            local targetPlayer = Players:FindFirstChild(selectedPlayerName)
            if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
                humanoidRootPart.CFrame = targetPlayer.Character.HumanoidRootPart.CFrame
            else
                print("Erro: Player alvo não encontrado ou sem HumanoidRootPart")
            end
        end
    })

    Troll:AddToggle({
        Name = "Spectar Player",
        Default = false,
        Callback = function(value)
            local Camera = workspace.CurrentCamera

            local function UpdateCamera()
                if value then
                    local targetPlayer = Players:FindFirstChild(selectedPlayerName)
                    if targetPlayer and targetPlayer.Character then
                        local humanoid = targetPlayer.Character:FindFirstChild("Humanoid")
                        if humanoid then
                            Camera.CameraSubject = humanoid
                        end
                    end
                else
                    if LocalPlayer.Character then
                        local humanoid = LocalPlayer.Character:FindFirstChild("Humanoid")
                        if humanoid then
                            Camera.CameraSubject = humanoid
                        end
                    end
                end
            end

            if value then
                if not getgenv().CameraConnection then
                    getgenv().CameraConnection = RunService.Heartbeat:Connect(UpdateCamera)
                end
            else
                if getgenv().CameraConnection then
                    getgenv().CameraConnection:Disconnect()
                    getgenv().CameraConnection = nil
                end
                UpdateCamera()
            end
        end
    })

    local MethodSection = Troll:AddSection({ Name = "Métodos" })

    local methodKill

Troll:AddDropdown({
    Name = "Select Kill Method",
    Options = {"Military Ship", "Couch", "Soccer Ball"},
    Default = "Soccer Ball",
    Callback = function(value)
        methodKill = value
        print("Método selecionado: " .. tostring(value))
    end
})

    Troll:AddButton({
        Name = "Matar Jogador",
        Callback = function()
            if not selectedPlayerName or not Players:FindFirstChild(selectedPlayerName) then
                print("Erro: Player não selecionado ou não existe")
                return
            end
        if methodKill == "Couch" then
                KillWithCouch()
            elseif methodKill == "Soccer Ball" then
                 FlingBall(game:GetService("Players")[selectedPlayerName])
      else
         if not selectedPlayerName or not game.Players:FindFirstChild(selectedPlayerName) then
            warn("Nenhum jogador selecionado ou não existe")
            return
        end

        local Player = game.Players.LocalPlayer
        local Character = Player.Character
        local Humanoid = Character and Character:FindFirstChildOfClass("Humanoid")
        local RootPart = Character and Character:FindFirstChild("HumanoidRootPart")
        local Vehicles = game.Workspace:FindFirstChild("Vehicles")

        if not Humanoid or not RootPart then
            warn("Humanoid ou RootPart inválido")
            return
        end

        local function spawnBoat()
            RootPart.CFrame = CFrame.new(1754, -2, 58)
            task.wait(0.5)
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Ca1r"):FireServer("PickingBoat", "MilitaryBoatFree")
            task.wait(1)
            return Vehicles:FindFirstChild(Player.Name.."Car")
        end

        local PCar = Vehicles:FindFirstChild(Player.Name.."Car") or spawnBoat()
        if not PCar then
            warn("Falha ao spawnar o barco")
            return
        end

        local Seat = PCar:FindFirstChild("Body") and PCar.Body:FindFirstChild("VehicleSeat")
        if not Seat then
            warn("Assento não encontrado")
            return
        end

        repeat 
            task.wait(0.1)
            RootPart.CFrame = Seat.CFrame * CFrame.new(0, 1, 0)
        until Humanoid.SeatPart == Seat

        print("Barco spawnado!")

        local TargetPlayer = game.Players:FindFirstChild(selectedPlayerName)
        if not TargetPlayer or not TargetPlayer.Character then
            warn("Jogador não encontrado")
            return
        end

        local TargetC = TargetPlayer.Character
        local TargetH = TargetC:FindFirstChildOfClass("Humanoid")
        local TargetRP = TargetC:FindFirstChild("HumanoidRootPart")

        if not TargetRP or not TargetH then
            warn("Humanoid ou RootPart do alvo não encontrado")
            return
        end

        local Spin = Instance.new("BodyAngularVelocity")
        Spin.Name = "Spinning"
        Spin.Parent = PCar.PrimaryPart
        Spin.MaxTorque = Vector3.new(0, math.huge, 0)
        Spin.AngularVelocity = Vector3.new(0, 369, 0) 

        print("Fling ativo!")

        local function moveCar(TargetRP, offset)
            if PCar and PCar.PrimaryPart then
                PCar:SetPrimaryPartCFrame(CFrame.new(TargetRP.Position + offset))
            end
        end

        task.spawn(function()
            while PCar and PCar.Parent and TargetRP and TargetRP.Parent do
                task.wait(0.01) 
                
                moveCar(TargetRP, Vector3.new(0, 1, 0))  
                moveCar(TargetRP, Vector3.new(0, -2.25, 5))  
                moveCar(TargetRP, Vector3.new(0, 2.25, 0.25))  
                moveCar(TargetRP, Vector3.new(-2.25, -1.5, 2.25))  
                moveCar(TargetRP, Vector3.new(0, 1.5, 0))  
                moveCar(TargetRP, Vector3.new(0, -1.5, 0))  

                if PCar and PCar.PrimaryPart then
                    local Rotation = CFrame.Angles(
                        math.rad(math.random(-369, 369)),  
                        math.rad(math.random(-369, 369)), 
                        math.rad(math.random(-369, 369))
                    )
                    PCar:SetPrimaryPartCFrame(CFrame.new(TargetRP.Position + Vector3.new(0, 1.5, 0)) * Rotation)
                end
            end

            if Spin and Spin.Parent then
                Spin:Destroy()
                print("Fling desativado")
            end
        end)
      end
    end
  })

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local LocalPlayer = Players.LocalPlayer

local RE = ReplicatedStorage:WaitForChild("RE")
local ClearEvent = RE:FindFirstChild("1Clea1rTool1s")
local ToolEvent = RE:FindFirstChild("1Too1l")
local FireEvent = RE:FindFirstChild("1Gu1n")

local FlingSystem = { power = 1e16, damage = 9999999999999999999999999999998, interval = 0.02 }

local function clearTools()
    if ClearEvent then
        ClearEvent:FireServer("ClearAllTools")
    end
end

local function requestAssault()
    if ToolEvent then
        ToolEvent:InvokeServer("PickingTools", "Assault")
    end
end

local function hasWeapon()
    return LocalPlayer.Backpack:FindFirstChild("Assault") or (LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("Assault"))
end

local function equipWeapon()
    local weapon = LocalPlayer.Backpack:FindFirstChild("Assault")
    if weapon and LocalPlayer.Character then
        local humanoid = LocalPlayer.Character:FindFirstChild("Humanoid")
        if humanoid then
            humanoid:EquipTool(weapon)
            return true
        end
    end
    return false
end

local function getGunScript()
    if LocalPlayer.Character then
        local weapon = LocalPlayer.Character:FindFirstChild("Assault") or LocalPlayer.Backpack:FindFirstChild("Assault")
        if weapon then
            return weapon:FindFirstChild("GunScript_Local")
        end
    end
    return nil
end

local function executeShot(targetPart)
    local gunScript = getGunScript()
    if not gunScript or not targetPart or not FireEvent then return end

    local muzzle = gunScript:FindFirstChild("MuzzleEffect")
    local hit = gunScript:FindFirstChild("HitEffect")
    if not muzzle or not hit then return end

    local args = {
        targetPart,
        targetPart,
        Vector3.new(FlingSystem.power, FlingSystem.power, FlingSystem.power),
        targetPart.Position,
        muzzle,
        hit,
        0,
        0,
        { false },
        {
            FlingSystem.damage,
            Vector3.new(5000, 5000, 5000),
            BrickColor.new(29),
            0.25,
            Enum.Material.SmoothPlastic,
            0.25
        },
        true,
        false
    }

    FireEvent:FireServer(unpack(args))
end

local function getSelectedTarget()
    if not selectedPlayerName then return nil end
    local player = Players:FindFirstChild(selectedPlayerName)
    if player and player.Character then
        local humanoid = player.Character:FindFirstChild("Humanoid")
        local rootPart = player.Character:FindFirstChild("HumanoidRootPart")
        if humanoid and humanoid.Health > 0 and rootPart then
            return { player = player, part = rootPart }
        end
    end
    return nil
end

local function flingTarget()
    local target = getSelectedTarget()
    if not target then return end

    executeShot(target.part)

    local char = target.player.Character
    if not char then return end

    local head = char:FindFirstChild("Head")
    if head then executeShot(head) end

    local torso = char:FindFirstChild("Torso") or char:FindFirstChild("UpperTorso")
    if torso then executeShot(torso) end
end

local function maintainWeapon()
    if not hasWeapon() then
        clearTools()
        task.wait(0.1)
        requestAssault()
        task.wait(0.2)

        local attempts = 0
        while not hasWeapon() and attempts < 20 do
            task.wait(0.1)
            attempts = attempts + 1
        end

        if hasWeapon() then
            equipWeapon()
        end
    end
end

function Stephannythrow()
    maintainWeapon()
    task.spawn(function()
        while true do
            maintainWeapon()
            if hasWeapon() and getGunScript() then
                pcall(flingTarget)
            end
            task.wait(FlingSystem.interval)
        end
    end)
end

Troll:AddSection({Name = "Annoy (Stephanny)"})

Troll:AddButton({
  Name = "Admin Annoy [ Stephanny Throw v1 ]",
Description = "Completely disrupts the target player",
  Callback = function()
            Stephannythrow()
end
})
Troll:AddButton({
        Name = "Couch Annoy [ Stephanny Throw v2 ]",
        Callback = function()
         playerCorrupt()
   end
})

local kill = Troll:AddSection({Name = "Matar todo mundo"})

Troll:AddButton({
    Name = "Matar todos os Jogadores (Military Ship)",
    Callback = function()
        local Player = game.Players.LocalPlayer
    local Character = Player.Character
    local Humanoid = Character:FindFirstChildOfClass("Humanoid")
    local RootPart = Character:FindFirstChild("HumanoidRootPart")
    local Vehicles = game.Workspace:FindFirstChild("Vehicles")
    local OldPos = RootPart.CFrame
    local Angles = 0
    local PCar = Vehicles:FindFirstChild(Player.Name.."Car")
    
            if not PCar then  
                if RootPart then  
                    RootPart.CFrame = CFrame.new(1754, -2, 58)  
                    task.wait(0.5)  
                    game:GetService("ReplicatedStorage").RE:FindFirstChild("1Ca1r"):FireServer("PickingBoat", "MilitaryBoatFree")  
                    task.wait(0.5)  
                    PCar = Vehicles:FindFirstChild(Player.Name.."Car")  
                    task.wait(0.5)  
                    local Seat = PCar:FindFirstChild("Body") and PCar.Body:FindFirstChild("VehicleSeat")  
                    if Seat then  
                        repeat  
                            task.wait()  
                            RootPart.CFrame = Seat.CFrame * CFrame.new(0, math.random(-1, 1), 0)  
                        until Humanoid.Sit  
                    end  
                end  
            end  
      
            task.wait(0.5)  
            PCar = Vehicles:FindFirstChild(Player.Name.."Car")  
      
            if PCar then  
                if not Humanoid.Sit then  
                    local Seat = PCar:FindFirstChild("Body") and PCar.Body:FindFirstChild("VehicleSeat")  
                    if Seat then  
                        repeat  
                            task.wait()  
                            RootPart.CFrame = Seat.CFrame * CFrame.new(0, math.random(-1, 1), 0)  
                        until Humanoid.Sit  
                    end  
                end  
            end  
      
            local SpinGyro = Instance.new("BodyGyro")  
            SpinGyro.Parent = PCar.PrimaryPart  
            SpinGyro.MaxTorque = Vector3.new(1e7, 1e7, 1e7)  
            SpinGyro.P = 1e7  
            SpinGyro.CFrame = PCar.PrimaryPart.CFrame * CFrame.Angles(0, math.rad(90), 0)  
      
            local function flingPlayer(TargetC, TargetRP, TargetH)
    Angles = 0  
                local endTime = tick() + 1  
                while tick() < endTime do  
                    Angles = Angles + 100  
                    task.wait()  
      
                    local kill = function(alvo, pos, angulo)  
                        PCar:SetPrimaryPartCFrame(CFrame.new(alvo.Position) * pos * angulo)  
                    end  
      
                    kill(TargetRP, CFrame.new(0, 3, 0), CFrame.Angles(math.rad(Angles), 0, 0))  
                    kill(TargetRP, CFrame.new(0, -1.5, 2), CFrame.Angles(math.rad(Angles), 0, 0))  
                    kill(TargetRP, CFrame.new(2, 1.5, 2.25), CFrame.Angles(math.rad(50), 0, 0))  
                    kill(TargetRP, CFrame.new(-2.25, -1.5, 2.25), CFrame.Angles(math.rad(30), 0, 0))  
                    kill(TargetRP, CFrame.new(0, 1.5, 0), CFrame.Angles(math.rad(Angles), 0, 0))  
                    kill(TargetRP, CFrame.new(0, -1.5, 0), CFrame.Angles(math.rad(Angles), 0, 0))  
                end  
            end  
      
            for _, Target in pairs(game.Players:GetPlayers()) do  
                if Target ~= Player then  
                    local TargetC = Target.Character  
                    local TargetH = TargetC and TargetC:FindFirstChildOfClass("Humanoid")  
                    local TargetRP = TargetC and TargetC:FindFirstChild("HumanoidRootPart")  
      
                    if TargetC and TargetH and TargetRP then  
                        flingPlayer(TargetC, TargetRP, TargetH)  
                    end  
                end  
            end  
      
            task.wait(0.5)  
            PCar:SetPrimaryPartCFrame(CFrame.new(0, 0, 0))  
            task.wait(0.5)  
            Humanoid.Sit = false  
            task.wait(0.5)  
            RootPart.CFrame = OldPos  
      
            SpinGyro:Destroy()  
    end
})
Troll:AddButton({
    Name = "Matar todos os Jogadores (Soccer Ball)",
    Callback = function()
local player=game:GetService("Players").LocalPlayer
local SoccerBalls=workspace.WorkspaceCom["001_SoccerBalls"]
local MyBall=SoccerBalls:FindFirstChild("Soccer"..player.Name)

if not MyBall then
if not player.Backpack:FindFirstChild("SoccerBall") then
local args={[1]="PickingTools",[2]="SoccerBall"}
game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
task.wait()
player.Backpack.SoccerBall.Parent=player.Character
repeat MyBall=SoccerBalls:FindFirstChild("Soccer"..player.Name) task.wait() until MyBall
player.Character.SoccerBall.Parent=player.Backpack
task.wait()
else
player.Backpack.SoccerBall.Parent=player.Character
repeat MyBall=SoccerBalls:FindFirstChild("Soccer"..player.Name) task.wait() until MyBall
player.Character.SoccerBall.Parent=player.Backpack
end
end


for i,v in pairs(game.Players:GetPlayers()) do
if v~=game.Players.LocalPlayer then
local target=v
local TCharacter=target.Character or target.CharacterAdded:Wait()
local THumanoidRootPart=TCharacter:WaitForChild("HumanoidRootPart")
if not MyBall or not THumanoidRootPart then return end

for _,v in pairs(MyBall:GetChildren()) do
if v:IsA("BodyMover") then v:Destroy() end
end

local bodyVelocity=Instance.new("BodyVelocity")
bodyVelocity.Velocity=Vector3.new(9e8,9e8,9e8)
bodyVelocity.MaxForce=Vector3.new(1/0,1/0,1/0)
bodyVelocity.P=1e10
bodyVelocity.Parent=MyBall

local bv=Instance.new("BodyVelocity")
bv.Velocity=Vector3.new(9e8,9e8,9e8)
bv.MaxForce=Vector3.new(1/0,1/0,1/0)
bv.P=1e9
bv.Parent=THumanoidRootPart

local oldPos=THumanoidRootPart.Position
workspace.CurrentCamera.CameraSubject=THumanoidRootPart

repeat
local velocity=THumanoidRootPart.Velocity.Magnitude
local parts={}
for _,v in pairs(TCharacter:GetDescendants()) do
if v:IsA("BasePart") and v.CanCollide and not v.Anchored then table.insert(parts,v) end
end
for _,part in ipairs(parts) do
local pos_x=target.Character.HumanoidRootPart.Position.X
local pos_y=target.Character.HumanoidRootPart.Position.Y
local pos_z=target.Character.HumanoidRootPart.Position.Z
pos_x=pos_x+(target.Character.HumanoidRootPart.Velocity.X/1.5)
pos_y=pos_y+(target.Character.HumanoidRootPart.Velocity.Y/1.5)
pos_z=pos_z+(target.Character.HumanoidRootPart.Velocity.Z/1.5)
MyBall.CFrame=CFrame.new(pos_x,pos_y,pos_z)
task.wait(1/6000)
end
task.wait(1/6000)
until THumanoidRootPart.Velocity.Magnitude>5000 or TCharacter.Humanoid.Health==0 or target.Parent~=game.Players or THumanoidRootPart.Parent~=TCharacter or TCharacter~=target.Character

end
end

workspace.CurrentCamera.CameraSubject=game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart")
  end
})
local Tab = Window:MakeTab({"Sound All", "music"})

Tab:AddSection({"Sound All"})

Tab:AddParagraph({"Warn", "Everyone on the servers can hear the sound"})

local audios = {
    {Name = "I Ghost The down...", ID = 84663543883498},
    {Name = "Compre ONLINE", ID = 8747441609},
    {Name = "Meu nome é ???", ID = 7339658122},
    {Name = "FAZ O L!", ID = 94350012510206},
    {Name = "Uh Que Nojo", ID = 103440368630269},
    {Name = "Sai dai Lava Prato", ID = 101232400175829},
    {Name = "Seloko num compensa", ID = 78442476709262},
    --{Name = "Chimpanzini Bananini Funk", ID = 137148228908678},
    --{Name = "Candyland Tobu", ID = 118939739460633},
    {Name = "Meme do Dom pollo What the hell", ID = 100656590080703},
    {Name = "Não to entendendo nada Estourado", ID = 7962533987},
    {Name = "Cachorro Rindo", ID = 8449305114},
}

local selectedAudioID

Tab:AddTextBox({
    Name = "ID DO SOM",
    PlaceholderText = "Type Here...",
    Callback = function(value)
        selectedAudioID = tonumber(value)
    end
})

local audioNames = {}
for _, audio in ipairs(audios) do
    table.insert(audioNames, audio.Name)
end

Tab:AddDropdown({
    Name = "SELECIONAR SOM",
    Description = "Choose an audio from the list",
    Options = audioNames,
    Default = audioNames[1],
    Flag = "selected_audio",
    Callback = function(value)
        for _, audio in ipairs(audios) do
            if audio.Name == value then
                selectedAudioID = audio.ID
                break
            end
        end
    end
})

local audioLoop = false

Tab:AddSection({"Loop Sound"})

local function playLoopedAudio()
    while audioLoop do
        if selectedAudioID then
            local args = {
                [1] = game:GetService("Workspace"),
                [2] = selectedAudioID,
                [3] = 1,
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Gu1nSound1s"):FireServer(unpack(args))

            local sound = Instance.new("Sound")
            sound.SoundId = "rbxassetid://" .. selectedAudioID
            sound.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
            sound:Play()
        else
        end

        task.wait(0.5) 
    end
end

Tab:AddToggle({
    Name = "LOOP",
    Default = false,
    Flag = "audio_loop",
    Callback = function(value)
        audioLoop = value
        if audioLoop then
            task.spawn(playLoopedAudio) 
        end
    end
})

local function playAudio()
    if selectedAudioID then
        local args = {
            [1] = game:GetService("Workspace"),
            [2] = selectedAudioID,
            [3] = 1,
        }
        game:GetService("ReplicatedStorage").RE:FindFirstChild("1Gu1nSound1s"):FireServer(unpack(args))

        local sound = Instance.new("Sound")
        sound.SoundId = "rbxassetid://" .. selectedAudioID
        sound.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
        sound:Play()
    else
    end
end

Tab:AddButton({"Play Sound", function()
    playAudio()
end})

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local audioID = 6314880174

local function Audio_All_ClientSide(ID)
    local function CheckFolderAudioAll()
        local FolderAudio = workspace:FindFirstChild("Audio all client")
        if not FolderAudio then
            FolderAudio = Instance.new("Folder")
            FolderAudio.Name = "Audio all client"
            FolderAudio.Parent = workspace
        end
        return FolderAudio
    end

    local function CreateSound(ID)
        if type(ID) ~= "number" then
            return nil
        end

        local Folder_Audio = CheckFolderAudioAll()
        if Folder_Audio then
            local Sound = Instance.new("Sound")
            Sound.SoundId = "rbxassetid://" .. ID
            Sound.Volume = 1
            Sound.Looped = false
            Sound.Parent = Folder_Audio
            Sound:Play()
            task.wait(1) 
            Sound:Destroy()
        end
    end

    CreateSound(ID)
end

local function Audio_All_ServerSide(ID)
    if type(ID) ~= "number" then
        return nil
    end

    local GunSoundEvent = ReplicatedStorage:FindFirstChild("1Gu1nSound1s", true)
    if GunSoundEvent then
        GunSoundEvent:FireServer(workspace, ID, 1)
    end
end

Tab:AddToggle({
    Name = "EXPLODIR OUVIDO DE TODOS",
    Description = ".",
    Default = false,
    Flag = "audio_spam",
    Callback = function(value)
        getgenv().Audio_All_loop_fast = value

        while getgenv().Audio_All_loop_fast do
            Audio_All_ServerSide(audioID)
            task.spawn(function()
                Audio_All_ClientSide(audioID)
            end)
            task.wait(0.03) 
        end
    end
})
local CarTab = Window:MakeTab({ "Voar Com Seu Carro", "car" })
CarTab:AddButton({
    Name = "Fly Vehicle",
    Callback = function()
local Flymguiv2 = Instance.new("ScreenGui")
local Drag = Instance.new("Frame")
local FlyFrame = Instance.new("Frame")
local ddnsfbfwewefe = Instance.new("TextButton")
local Speed = Instance.new("TextBox")
local Fly = Instance.new("TextButton")
local Speeed = Instance.new("TextLabel")
local Stat = Instance.new("TextLabel")
local Stat2 = Instance.new("TextLabel")
local Unfly = Instance.new("TextButton")
local Vfly = Instance.new("TextLabel")
local Close = Instance.new("TextButton")
local Minimize = Instance.new("TextButton")
local Flyon = Instance.new("Frame")
local W = Instance.new("TextButton")
local S = Instance.new("TextButton")

Flymguiv2.Name = "Car Fly"
Flymguiv2.Parent = game.CoreGui
Flymguiv2.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Drag.Name = "Drag"
Drag.Parent = Flymguiv2
Drag.Active = true
Drag.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
Drag.BorderSizePixel = 0
Drag.Draggable = true
Drag.Position = UDim2.new(0.482438415, 0, 0.454874992, 0)
Drag.Size = UDim2.new(0, 237, 0, 27)

FlyFrame.Name = "FlyFrame"
FlyFrame.Parent = Drag
FlyFrame.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
FlyFrame.BorderSizePixel = 0
FlyFrame.Draggable = true
FlyFrame.Position = UDim2.new(-0.00200000009, 0, 0.989000022, 0)
FlyFrame.Size = UDim2.new(0, 237, 0, 139)

Speed.Name = "Speed"
Speed.Parent = FlyFrame
Speed.BackgroundColor3 = Color3.fromRGB(63, 63, 63)
Speed.BorderColor3 = Color3.fromRGB(0, 0, 191)
Speed.BorderSizePixel = 0
Speed.Position = UDim2.new(0.445025861, 0, 0.402877688, 0)
Speed.Size = UDim2.new(0, 111, 0, 33)
Speed.Font = Enum.Font.SourceSans
Speed.PlaceholderColor3 = Color3.fromRGB(255, 255, 255)
Speed.Text = "50"
Speed.TextColor3 = Color3.fromRGB(255, 255, 255)
Speed.TextScaled = true
Speed.TextSize = 14.000
Speed.TextWrapped = true

Fly.Name = "Fly"
Fly.Parent = FlyFrame
Fly.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
Fly.BorderSizePixel = 0
Fly.Position = UDim2.new(0.0759493634, 0, 0.705797076, 0)
Fly.Size = UDim2.new(0, 199, 0, 32)
Fly.Font = Enum.Font.SourceSans
Fly.Text = "kitk4t BAZUCA LINDO"
Fly.TextColor3 = Color3.fromRGB(255, 255, 255)
Fly.TextScaled = true
Fly.TextSize = 14.000
Fly.TextWrapped = true
Fly.MouseButton1Click:Connect(function()
	local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
	Fly.Visible = false
	Stat2.Text = "On"
	Stat2.TextColor3 = Color3.fromRGB(0, 255, 0)
	Unfly.Visible = true
	Flyon.Visible = true
	local BV = Instance.new("BodyVelocity",HumanoidRP)
	local BG = Instance.new("BodyGyro",HumanoidRP)
	BV.MaxForce = Vector3.new(math.huge,math.huge,math.huge)
	game:GetService('RunService').RenderStepped:connect(function()
	BG.MaxTorque = Vector3.new(math.huge,math.huge,math.huge)
	BG.D = 5000
	BG.P = 100000
	BG.CFrame = game.Workspace.CurrentCamera.CFrame
	end)
end)

Speeed.Name = "Speeed"
Speeed.Parent = FlyFrame
Speeed.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
Speeed.BorderSizePixel = 0
Speeed.Position = UDim2.new(0.0759493634, 0, 0.402877688, 0)
Speeed.Size = UDim2.new(0, 87, 0, 32)
Speeed.ZIndex = 0
Speeed.Font = Enum.Font.SourceSans
Speeed.Text = "KITK4T X HUB"
Speeed.TextColor3 = Color3.fromRGB(255, 255, 255)
Speeed.TextScaled = true
Speeed.TextSize = 14.000
Speeed.TextWrapped = true

Stat.Name = "Stat"
Stat.Parent = FlyFrame
Stat.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
Stat.BorderSizePixel = 0
Stat.Position = UDim2.new(0.299983799, 0, 0.239817441, 0)
Stat.Size = UDim2.new(0, 85, 0, 15)
Stat.Font = Enum.Font.SourceSans
Stat.Text = "KITK4T X HUB:"
Stat.TextColor3 = Color3.fromRGB(255, 255, 255)
Stat.TextScaled = true
Stat.TextSize = 14.000
Stat.TextWrapped = true

Stat2.Name = "Stat2"
Stat2.Parent = FlyFrame
Stat2.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
Stat2.BorderSizePixel = 0
Stat2.Position = UDim2.new(0.546535194, 0, 0.239817441, 0)
Stat2.Size = UDim2.new(0, 27, 0, 15)
Stat2.Font = Enum.Font.SourceSans
Stat2.Text = "Off"
Stat2.TextColor3 = Color3.fromRGB(255, 0, 0)
Stat2.TextScaled = true
Stat2.TextSize = 14.000
Stat2.TextWrapped = true

Unfly.Name = "Unfly"
Unfly.Parent = FlyFrame
Unfly.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
Unfly.BorderSizePixel = 0
Unfly.Position = UDim2.new(0.0759493634, 0, 0.705797076, 0)
Unfly.Size = UDim2.new(0, 199, 0, 32)
Unfly.Visible = false
Unfly.Font = Enum.Font.SourceSans
Unfly.Text = "KITK4T X HUB"
Unfly.TextColor3 = Color3.fromRGB(255, 255, 255)
Unfly.TextScaled = true
Unfly.TextSize = 14.000
Unfly.TextWrapped = true
Unfly.MouseButton1Click:Connect(function()
	local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
	Fly.Visible = true
	Stat2.Text = "Off"
	Stat2.TextColor3 = Color3.fromRGB(255, 0, 0)
	wait()
	Unfly.Visible = false
	Flyon.Visible = false
	HumanoidRP:FindFirstChildOfClass("BodyVelocity"):Destroy()
	HumanoidRP:FindFirstChildOfClass("BodyGyro"):Destroy()
end)

Vfly.Name = "Vfly"
Vfly.Parent = Drag
Vfly.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
Vfly.BorderSizePixel = 0
Vfly.Size = UDim2.new(0, 57, 0, 27)
Vfly.Font = Enum.Font.SourceSans
Vfly.Text = "CREDITOS: X HUB BROOKHAVEN"
Vfly.TextColor3 = Color3.fromRGB(255, 255, 255)
Vfly.TextScaled = true
Vfly.TextSize = 14.000
Vfly.TextWrapped = true

Close.Name = "Close"
Close.Parent = Drag
Close.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
Close.BorderSizePixel = 0
Close.Position = UDim2.new(0.875, 0, 0, 0)
Close.Size = UDim2.new(0, 27, 0, 27)
Close.Font = Enum.Font.SourceSans
Close.Text = "BAZUCA LINDO"
Close.TextColor3 = Color3.fromRGB(255, 255, 255)
Close.TextScaled = true
Close.TextSize = 14.000
Close.TextWrapped = true
Close.MouseButton1Click:Connect(function()
	Flymguiv2:Destroy()
end)

Minimize.Name = "Minimize"
Minimize.Parent = Drag
Minimize.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
Minimize.BorderSizePixel = 0
Minimize.Position = UDim2.new(0.75, 0, 0, 0)
Minimize.Size = UDim2.new(0, 27, 0, 27)
Minimize.Font = Enum.Font.SourceSans
Minimize.Text = "-"
Minimize.TextColor3 = Color3.fromRGB(255, 255, 255)
Minimize.TextScaled = true
Minimize.TextSize = 14.000
Minimize.TextWrapped = true
function Mini()
	if Minimize.Text == "-" then
		Minimize.Text = "+"
		FlyFrame.Visible = false
	elseif Minimize.Text == "+" then
		Minimize.Text = "-"
		FlyFrame.Visible = true
	end
end
Minimize.MouseButton1Click:Connect(Mini)

Flyon.Name = "Fly on"
Flyon.Parent = Flymguiv2
Flyon.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Flyon.BorderSizePixel = 0
Flyon.Position = UDim2.new(0.117647067, 0, 0.550284624, 0)
Flyon.Size = UDim2.new(0.148000002, 0, 0.314999998, 0)
Flyon.Visible = false
Flyon.Active = true
Flyon.Draggable = true

W.Name = "W"
W.Parent = Flyon
W.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
W.BorderSizePixel = 0
W.Position = UDim2.new(0.134719521, 0, 0.0152013302, 0)
W.Size = UDim2.new(0.708999991, 0, 0.499000013, 0)
W.Font = Enum.Font.SourceSans
W.Text = "^"
W.TextColor3 = Color3.fromRGB(255, 255, 255)
W.TextScaled = true
W.TextSize = 14.000
W.TextWrapped = true
W.TouchLongPress:Connect(function()
	local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * 0
end)

W.MouseButton1Click:Connect(function()
	local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * 0
end)

S.Name = "S"
S.Parent = Flyon
S.BackgroundColor3 = Color3.fromRGB(0, 150, 191)
S.BorderSizePixel = 0
S.Position = UDim2.new(0.134000003, 0, 0.479999989, 0)
S.Rotation = 180.000
S.Size = UDim2.new(0.708999991, 0, 0.499000013, 0)
S.Font = Enum.Font.SourceSans
S.Text = "^"
S.TextColor3 = Color3.fromRGB(255, 255, 255)
S.TextScaled = true
S.TextSize = 14.000
S.TextWrapped = true
S.TouchLongPress:Connect(function()
	local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * 0
end)

S.MouseButton1Click:Connect(function()
	local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed.Text
	wait(.1)
	HumanoidRP.BodyVelocity.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * 0
end)
    end
})
local LocalPlayerTab = Window:MakeTab({"Chat", "user"})


Section = LocalPlayerTab:AddSection({
    Name = "Chat"
})

local TextSave
local tcs = game:GetService("TextChatService")
local chat = tcs.ChatInputBarConfiguration and tcs.ChatInputBarConfiguration.TargetTextChannel

function sendchat(msg)
    if not msg or msg == "" then return end
    if tcs.ChatVersion == Enum.ChatVersion.LegacyChatService then
        local success, err = pcall(function()
            game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents").SayMessageRequest:FireServer(msg, "All")
        end)
        if not success then
        end
    elseif chat then
        local success, err = pcall(function()
            chat:SendAsync(msg)
        end)
        if not success then
        end
    end
end

LocalPlayerTab:AddTextBox({
    Name = "Enter Text",
    PlaceholderText = "Uh... Hi!",
    Callback = function(text)
        TextSave = text
    end
})

LocalPlayerTab:AddButton({
    Name = "Send Chat",
    Callback = function()
        sendchat(TextSave)
    end
})

getgenv().ChaosHubEnviarDelay = 1

LocalPlayerTab:AddSlider({
    Name = "Delay Spam",
    Min = 0.4,
    Max = 10,
    Default = 1,
    Increment = 0.1,
    Callback = function(Value)
        getgenv().ChaosHubEnviarDelay = Value
    end
})

LocalPlayerTab:AddToggle({
    Name = "Spam Chat",
    Default = false,
    Flag = "SpamXhati",
    Callback = function(Value)
        getgenv().ChaosHubSpawnText = Value
        while getgenv().ChaosHubSpawnText do
            sendchat(TextSave)
            task.wait(getgenv().ChaosHubEnviarDelay)
        end
    end
})

LocalPlayerTab:AddButton({
    Name = "Spam Chat - Hacked by X Hub",
    Callback = function()
        if game:GetService("TextChatService").ChatVersion == Enum.ChatVersion.TextChatService then 
            game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("hi\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\r\rSystem: Hacked by X Hub")
        else 
    end
end
})

LocalPlayerTab:AddButton({
    Name = "Clear Chat",
    Callback = function()
        if game:GetService("TextChatService").ChatVersion == Enum.ChatVersion.TextChatService then 
            game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("hi\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\nn\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\nServer: Chat Cleared by X Hub")
        else 
    end
end
})
local Tab = Window:MakeTab({"Avatar", "rbxassetid://10734952036"})

Tab:AddSection({ Name = "Avatar" })

Tab:AddSection({ Name = "Copy Avatar" })
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Remotes = ReplicatedStorage:WaitForChild("Remotes")

local Target = nil

local function GetPlayerNames()
    local PlayerNames = {}
    for _, player in ipairs(Players:GetPlayers()) do
        table.insert(PlayerNames, player.Name)
    end
    return PlayerNames
end

local Dropdown = Tab:AddDropdown({
    Name = "Select Player",
    Options = GetPlayerNames(),
    Default = Target,
    Callback = function(Value)
        Target = Value
    end
})

local function UpdateDropdown()
    Dropdown:Refresh(GetPlayerNames(), true)
end

Players.PlayerAdded:Connect(UpdateDropdown)
Players.PlayerRemoving:Connect(UpdateDropdown)

Tab:AddButton({
    Name = "Copy Avatar",
    Callback = function()
        if not Target then return end

        local LP = Players.LocalPlayer
        local LChar = LP.Character
        local TPlayer = Players:FindFirstChild(Target)

        if TPlayer and TPlayer.Character then
            local LHumanoid = LChar and LChar:FindFirstChildOfClass("Humanoid")
            local THumanoid = TPlayer.Character:FindFirstChildOfClass("Humanoid")

            if LHumanoid and THumanoid then
                local LDesc = LHumanoid:GetAppliedDescription()

                for _, acc in ipairs(LDesc:GetAccessories(true)) do
                    if acc.AssetId and tonumber(acc.AssetId) then
                        Remotes.Wear:InvokeServer(tonumber(acc.AssetId))
                        task.wait(0.2)
                    end
                end

                if tonumber(LDesc.Shirt) then
                    Remotes.Wear:InvokeServer(tonumber(LDesc.Shirt))
                    task.wait(0.2)
                end

                if tonumber(LDesc.Pants) then
                    Remotes.Wear:InvokeServer(tonumber(LDesc.Pants))
                    task.wait(0.2)
                end

                if tonumber(LDesc.Face) then
                    Remotes.Wear:InvokeServer(tonumber(LDesc.Face))
                    task.wait(0.2)
                end

                local PDesc = THumanoid:GetAppliedDescription()

                local argsBody = {
                    [1] = {
                        [1] = PDesc.Torso,
                        [2] = PDesc.RightArm,
                        [3] = PDesc.LeftArm,
                        [4] = PDesc.RightLeg,
                        [5] = PDesc.LeftLeg,
                        [6] = PDesc.Head
                    }
                }
                Remotes.ChangeCharacterBody:InvokeServer(unpack(argsBody))
                task.wait(0.5)

                if tonumber(PDesc.Shirt) then
                    Remotes.Wear:InvokeServer(tonumber(PDesc.Shirt))
                    task.wait(0.3)
                end

                if tonumber(PDesc.Pants) then
                    Remotes.Wear:InvokeServer(tonumber(PDesc.Pants))
                    task.wait(0.3)
                end

                if tonumber(PDesc.Face) then
                    Remotes.Wear:InvokeServer(tonumber(PDesc.Face))
                    task.wait(0.3)
                end

                for _, v in ipairs(PDesc:GetAccessories(true)) do
                    if v.AssetId and tonumber(v.AssetId) then
                        Remotes.Wear:InvokeServer(tonumber(v.AssetId))
                        task.wait(0.3)
                    end
                end

                local SkinColor = TPlayer.Character:FindFirstChild("Body Colors")
                if SkinColor then
                    Remotes.ChangeBodyColor:FireServer(tostring(SkinColor.HeadColor))
                    task.wait(0.3)
                end

                if tonumber(PDesc.IdleAnimation) then
                    Remotes.Wear:InvokeServer(tonumber(PDesc.IdleAnimation))
                    task.wait(0.3)
                end

                local Bag = TPlayer:FindFirstChild("PlayersBag")
                if Bag then
                    if Bag:FindFirstChild("RPName") and Bag.RPName.Value ~= "" then
                        Remotes.RPNameText:FireServer("RolePlayName", Bag.RPName.Value)
                        task.wait(0.3)
                    end
                    if Bag:FindFirstChild("RPBio") and Bag.RPBio.Value ~= "" then
                        Remotes.RPNameText:FireServer("RolePlayBio", Bag.RPBio.Value)
                        task.wait(0.3)
                    end
                    if Bag:FindFirstChild("RPNameColor") then
                        Remotes.RPNameColor:FireServer("PickingRPNameColor", Bag.RPNameColor.Value)
                        task.wait(0.3)
                    end
                    if Bag:FindFirstChild("RPBioColor") then
                        Remotes.RPNameColor:FireServer("PickingRPBioColor", Bag.RPBioColor.Value)
                        task.wait(0.3)
                    end
                end
            end
        end
    end
})


	end)
