_G.Set = true
_G.M = true

spawn(function()
   while wait(0.1) do
      if _G.Set then
         pcall(function()
         local args = {
         [1] = "SetSpawnPoint"
         }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
      end)
    end
  end
end)

function TpFarm() 
MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
if MyLevel == 10 then
   game:GetService("Players").LocalPlayer.Character.Humanoid.Health = 0
   wait(0.1)
   game .Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1612.79578, 37.195343, 149.128433, 1, 0, 0, 0, 1, 0, 0, 0, 1)
   wait(90)
elseif MyLevel == 25 or MyLevel <= 99 then
    wait(0.10)
   game:GetService("Players").LocalPlayer.Character.Humanoid.Health = 0
   wait(0.1)
   game .Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
   wait(900)
elseif MyLevel == 100 then
    wait(0.10)
   game:GetService("Players").LocalPlayer.Character.Humanoid.Health = 0
   wait(0.1)
   game .Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
   wait(90)
   end
end

 while wait() do
     if _G.M then
 pcall(function()
TpFarm() 
              end)
           end
    end
