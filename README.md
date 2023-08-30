game:GetService("StarterGui"):SetCore("SendNotification",{
    Title = "quracik",
    Text = "Made By quracik",
    Icon = "rbxassetid://57254792";
Duration = 5;
})
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Gamepass, Qura W Pyth", "Ocean")
    -- MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")

local AnimationCurveLoop

MainSection:NewToggle("More Curve", "The Ball Curves More", function(arg)
if arg then
game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.WoodenFloor.Tick.Visible = true
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.WoodenFloor.WoodenFloor.Style = "RobloxRoundButton"

local Humanoid = game.Players.LocalPlayer.Character.Humanoid

AnimationCurveLoop = Humanoid.AnimationPlayed:Connect(function(AnimationTrack)
    if AnimationTrack.Name == "OldMKickL" or AnimationTrack.Name == "OldMKick" or AnimationTrack.Name == "OldLKickL" or AnimationTrack.Name == "OldLKick" or AnimationTrack.Name == "MKickL" or AnimationTrack.Name == "MKick" or AnimationTrack.Name == "LKickL" or AnimationTrack.Name == "LKick" or AnimationTrack.Name == "OldDribbleL" or AnimationTrack.Name == "OldDribble" or AnimationTrack.Name == "DribbleL" or AnimationTrack.Name == "Dribble" then
    if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game.Workspace.TPSSystem.TPS.Position).Magnitude < 3.45 then
        if game.Players.LocalPlayer.Backpack.Curving.Value == 2 then
        wait(0.1)
                local A_1T = game:GetService("Workspace").TPSSystem.TPS
local A_2T = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
local EventT = game:GetService("Workspace").FE.Actions.KickC1
EventT:FireServer(A_1T, A_2T)
wait(0.2)
EventT:FireServer(A_1T, A_2T)

elseif game.Players.LocalPlayer.Backpack.Curving.Value == 1 then
wait(0.1)
local A_1 = game:GetService("Workspace").TPSSystem.TPS
local A_2 = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
local Event = game:GetService("Workspace").FE.Actions.KickC2
Event:FireServer(A_1, A_2)
wait(0.2)
Event:FireServer(A_1, A_2)

            end
        end
    end
end)
    else
        AnimationCurveLoop:Disconnect()
        game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.WoodenFloor.Tick.Visible = false
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.WoodenFloor.WoodenFloor.Style = "RobloxRoundDefaultButton"
    end
end)

MainSection:NewToggle("Blue Flame", "Flame Color Effect Will Be Blue Now.", function(arg)
if arg then
game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.BlueFlame.Tick.Visible = true
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.BlueFlame.BlueFlame.Style = "RobloxRoundButton"
        game:GetService("Players").LocalPlayer.PlayerGui.Start.PowerShot.Image = "rbxassetid://5366457711"
        game:GetService("Players").LocalPlayer.Backpack.FValue.Value = 2
    else
        game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.BlueFlame.Tick.Visible = false
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.BlueFlame.BlueFlame.Style = "RobloxRoundDefaultButton"
        game:GetService("Players").LocalPlayer.PlayerGui.Start.PowerShot.Image = "rbxassetid://1595877615"
       game:GetService("Players").LocalPlayer.Backpack.FValue.Value = 1
    end
end)

MainSection:NewToggle("Frozen Ball", "Freezes The Flame Ball When It Touched You. Ice Is NON-FE", function(arg)
if arg then
game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Frozen.Tick.Visible = true
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Frozen.Frozen.Style = "RobloxRoundButton"
    
_G.FROZEN = true
    while _G.FROZEN do
    wait()
        game:GetService("Players").LocalPlayer.Backpack.Frozen.Value = true
        for i,v in pairs(game.Workspace:GetDescendants()) do
    if v.Name == "TPS" and v:IsA("Part") then
    if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude <= 5 then
    if v.Fire.Enabled == true or v.FireB.Enabled == true then
       v.BrickColor = BrickColor.new("Cyan")
       local A_1 = game:GetService("Workspace").TPSSystem.TPS
local A_2 = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
local A_3 = 0
local A_4 = Vector3.new(4000000, 300, 4000000)
local Event = game:GetService("Workspace").FE.Actions.KickG1
Event:FireServer(A_1, A_2, A_3, A_4)
wait(.1)
local A_1 = game:GetService("Workspace").TPSSystem.TPS
local A_2 = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
local A_3 = 0
local A_4 = Vector3.new(4000000, 300, 4000000)
local Event = game:GetService("Workspace").FE.Actions.KickG1
Event:FireServer(A_1, A_2, A_3, A_4)
wait(2.4)
v.BrickColor = BrickColor.new("Institutional white")
    end
    end
    end
    end
    end
    else
     game:GetService("Players").LocalPlayer.Backpack.Frozen.Value = false
     _G.FROZEN = false
     game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Frozen.Tick.Visible = false
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Frozen.Frozen.Style = "RobloxRoundDefaultButton"
    end
end)

MainSection:NewToggle("Faster Cooldown", "Reduces The Power Show Cooldown By 50% (30)", function(arg)
if arg then
game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Cooldown.Tick.Visible = true
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Cooldown.Cooldown.Style = "RobloxRoundButton"
        game:GetService("Players").LocalPlayer.PlayerGui.Start.PowerShot.PowerValue.Value = 30
    else
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Cooldown.Cooldown.Style = "RobloxRoundDefaultButton"
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.Cooldown.Tick.Visible = false
       game:GetService("Players").LocalPlayer.PlayerGui.Start.PowerShot.PowerValue.Value = 60
    end
end)

local AnimationTackleLoop

MainSection:NewToggle("Powerful Tackle", "Your Tackle Will Be Powerful. Very Buggy - Don't Recommend To Use", function(arg)
if arg then
game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.RandomWeather.Tick.Visible = true
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.RandomWeather.RandomWeather.Style = "RobloxRoundButton"
        game:GetService("Players").LocalPlayer.PlayerGui.Start.TackleGamePass.Value = true
        
        local Humanoid = game.Players.LocalPlayer.Character.Humanoid

AnimationTackleLoop = Humanoid.AnimationPlayed:Connect(function(AnimationTrack)
    if AnimationTrack.Name == "TackleL" or AnimationTrack.Name == "Tackle" or AnimationTrack.Name == "OldTackleL" or AnimationTrack.Name == "OldTackle" then
    if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game.Workspace.TPSSystem.TPS.Position).Magnitude < 4.87 then
        wait(0.8)
                local A_1 = game:GetService("Workspace").TPSSystem.TPS
local A_2 = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
local A_3 = 30
local A_4 = Vector3.new(4000000, 700, 4000000)
local Event = game:GetService("Workspace").FE.Actions.KickG1
Event:FireServer(A_1, A_2, A_3, A_4)

        end
    end
end)
    else
      game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.RandomWeather.Tick.Visible = false
    game:GetService("Players").LocalPlayer.PlayerGui.Start.GamePassMenu.Items.RandomWeather.RandomWeather.Style = "RobloxRoundDefaultButton"
      game:GetService("Players").LocalPlayer.PlayerGui.Start.TackleGamePass.Value = false
      AnimationTackleLoop:Disconnect()
    end
end)
