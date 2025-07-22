# Jarlan_v3..
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = LocalPlayer:WaitForChild("PlayerGui")

local Botao = Instance.new("TextButton")
Botao.Size = UDim2.new(0,200,0,50)
Botao.Position = UDim2.new(0.5,-100,0.9,-25)
Botao.Text = "TP + Speed + Jump"
Botao.BackgroundColor3 = Color3.fromRGB(0,170,255)
Botao.Parent = ScreenGui

Botao.MouseButton1Click:Connect(function()
    local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local HRP = Character:WaitForChild("HumanoidRootPart")
    local Humanoid = Character:WaitForChild("Humanoid")

    -- ajusta aqui pra posição da base
    HRP.CFrame = CFrame.new(0,150,0)

    -- speed & jump
    Humanoid.WalkSpeed = 60
    Humanoid.JumpPower = 100
end)
