if game.PlaceId == 155615604 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Prison Life", "Ocean")

    -- MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")


     -- PLAYER
     local Player = Window:NewTab("Player")
     local PlayerSection = Player:NewSection("Player")
 
     PlayerSection:NewSlider("Walkspeed", "Changes the walkspeed", 250, 16, function(v)
         game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
     end)
 
     PlayerSection:NewSlider("Jumppower", "Changes the jumppower", 250, 50, function(v)
         game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
     end)
 elseif game.PlaceId == 3956818381 then
     local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
     local Window = Library.CreateLib("Ninja Legends", "Ocean")
 
     -- MAIN
     local Main = Window:NewTab("Main")
     local MainSection = Main:NewSection("Main")
 
     MainSection:NewToggle("Auto Swing", "Make your player autoswing", function(v)
         getgenv().autoswing = v
         while true do
             if not getgenv().autoswing then return end
             for _,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                 if v:FindFirstChild("ninjitsuGain") then
                     game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                     break
                 end
             end
             local A_1 = "swingKatana"
             local Event = game:GetService("Players").LocalPlayer.ninjaEvent
             Event:FireServer(A_1)
             wait(0.1)
         end
     end)
 
     MainSection:NewToggle("Auto Sell", "Makes your player autosell", function(v)
         getgenv().autosell = v
         while true do
             if getgenv().autoswing == false then return end
             game:GetService("Workspace").sellAreaCircles["sellAreaCircle16"].circleInner.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
             wait(0.1)
             game:GetService("Workspace").sellAreaCircles["sellAreaCircle16"].circleInner.CFrame = CFrame.new(0,0,0)
             wait(0.1)
         end
     end)
 
     MainSection:NewButton("Unlock all islands", "Unlocks all islands", function()
         local oldcframe = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
         for _,v in pairs(game:GetService("Workspace").islandUnlockParts:GetChildren()) do
             game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
             wait(0.1)
         end
         wait(0.1)
         game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = oldcframe
     end)
     
     MainSection:NewToggle("Auto buy all swords", "Auto buys all swords", function(v)
         getgenv().buyswords = v
         while true do
             if not getgenv().buyswords then return end
             local A_1 = "buyAllSwords"
             local A_2 = "Inner Peace Island"
             local Event = game:GetService("Players").LocalPlayer.ninjaEvent
             Event:FireServer(A_1, A_2)
             wait(0.5)
         end
     end)
 
     MainSection:NewToggle("Auto buy all belts", "Auto buys all belts", function(v)
         getgenv().buybelts = v
         while true do
             if not getgenv().buybelts then return end
             local A_1 = "buyAllBelts"
             local A_2 = "Inner Peace Island"
             local Event = game:GetService("Players").LocalPlayer.ninjaEvent
             Event:FireServer(A_1, A_2)
             wait(0.5)
         end
     end)
 end

 if game.PlaceId == 4952780297 then
    local Library = loadstring(game:HttpGet('https://raw.githubusercontent.com/s2mikeyzz/rbxscript/main/CombatRift.lua', true))()
   end

   if game.PlaceId == 286090429 then
      local Library = loadstring(game:HttpGet('https://raw.githubusercontent.com/NougatBitz/DuckHub/master/Main.lua'))()
   end

   if game.PlaceId == 621129760 then
    local Library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/mememasterboi/a-lot-of-scripts/master/Output%20(6).lua'),true))()
   end
