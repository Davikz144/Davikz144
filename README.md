local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

local button = script.Parent

local teleportFolder = workspace:WaitForChild("Teleports")
local destino = teleportFolder:WaitForChild("1")

if button and button:IsA("TextButton") then
	button.MouseButton1Click:Connect(function()
		if humanoidRootPart then
			humanoidRootPart.CFrame = destino.CFrame + Vector3.new(0, 3, 0)
		end
	end)
else
	warn("kk")
end
