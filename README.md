function FlyRoblox(player)
    local humanoid = player.Character:WaitForChild("Humanoid")
    local rootPart = player.Character:WaitForChild("HumanoidRootPart")
    local flySpeed = 50
    local flyKey = Enum.KeyCode.Space

    game:GetService("UserInputService").InputBegan:Connect(function(input)
        if input.KeyCode == flyKey then
            humanoid.Sit = true
            wait()
            rootPart.Velocity = Vector3.new(0, flySpeed, 0)
        end
    end)
end

FlyRoblox(game.Players.LocalPlayer)
