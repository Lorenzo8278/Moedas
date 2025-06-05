-- Criação da Interface
local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local CoinButton = Instance.new("TextButton")
local CoinCountLabel = Instance.new("TextLabel")

local player = game.Players.LocalPlayer
local PlayerGui = player:WaitForChild("PlayerGui")

ScreenGui.Name = "CoinHackUI"
ScreenGui.Parent = PlayerGui

-- Frame principal
MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
MainFrame.Position = UDim2.new(0.65, 0, 0.2, 0)
MainFrame.Size = UDim2.new(0, 300, 0, 200)
MainFrame.Active = true
MainFrame.Draggable = true

-- Título
Title.Name = "Title"
Title.Parent = MainFrame
Title.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
Title.Size = UDim2.new(1, 0, 0.2, 0)
Title.Font = Enum.Font.SourceSansBold
Title.Text = "Sistema de Moedas"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true

-- Botão de Pegar Moedas
CoinButton.Name = "CoinButton"
CoinButton.Parent = MainFrame
CoinButton.BackgroundColor3 = Color3.fromRGB(30, 120, 30)
CoinButton.Position = UDim2.new(0.15, 0, 0.5, 0)
CoinButton.Size = UDim2.new(0.7, 0, 0.2, 0)
CoinButton.Font = Enum.Font.SourceSansBold
CoinButton.Text = "PEGAR MOEDAS"
CoinButton.TextColor3 = Color3.fromRGB(255, 255, 255)
CoinButton.TextScaled = true

-- Contador de moedas
CoinCountLabel.Name = "CoinCountLabel"
CoinCountLabel.Parent = MainFrame
CoinCountLabel.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
CoinCountLabel.Position = UDim2.new(0.15, 0, 0.75, 0)
CoinCountLabel.Size = UDim2.new(0.7, 0, 0.15, 0)
CoinCountLabel.Font = Enum.Font.SourceSans
CoinCountLabel.Text = "Moedas: 0"
CoinCountLabel.TextColor3 = Color3.fromRGB(255, 255, 0)
CoinCountLabel.TextScaled = true

-- Variável de moedas
local moedas = 0

-- Função ao clicar
CoinButton.MouseButton1Click:Connect(function()
    moedas = moedas + 100
    CoinCountLabel.Text = "Moedas: " .. moedas
end)
