local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()
----------------------------------------------------------------------------------------------------------------------------------------------
local Window = Fluent:CreateWindow({
    Title = "Maruko Hub",
    SubTitle = "By x_2Swiftz",
    TabWidth = 160,
    Size = UDim2.fromOffset(500, 320),
    Acrylic = false,
    Theme = "Amethyst",
    MinimizeKey = Enum.KeyCode.End
})
local Tabs = {
    Main = Window:AddTab({ Title = "Main", Icon = "home" }),
    Stats = Window:AddTab({ Title = "Stats", Icon = "plus-circle" }),
    Setting = Window:AddTab({ Title = "Settings", Icon = "Settings" }),
    
}
local Options = Fluent.Options
do
--------------------------------------------------------------------------------------------------------------------------------------------
--// Place Id Check
local id = game.PlaceId
if id == 2753915549 then First_Sea = true; elseif id == 4442272183 then Second_Sea = true; elseif id == 7449423635 then Third_Sea = true; else game:Shutdown() end;
--------------------------------------------------------------------------------------------------------------------------------------------
--// Flag Player
function AntiBan()
    for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetDescendants()) do
        if v:IsA("LocalScript") then
            if v.Name == "General" or v.Name == "Shiftlock"  or v.Name == "FallDamage" or v.Name == "4444" or v.Name == "CamBob" or v.Name == "JumpCD" or v.Name == "Looking" or v.Name == "Run" then
                v:Destroy()
            end
        end
     end
     for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerScripts:GetDescendants()) do
        if v:IsA("LocalScript") then
            if v.Name == "RobloxMotor6DBugFix" or v.Name == "Clans"  or v.Name == "Codes" or v.Name == "CustomForceField" or v.Name == "MenuBloodSp"  or v.Name == "PlayerList" then
                v:Destroy()
            end
        end
     end
    end
    AntiBan()
--------------------------------------------------------------------------------------------------------------------------------------------
--// Anti AFK
game:GetService("Players").LocalPlayer.Idled:connect(function()
	game:GetService("VirtualUser"):Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
	wait(1)
	game:GetService("VirtualUser"):Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)
-------------// BLOX FRUIT
--// Sea World
First_Sea = false
Second_Sea = false
Third_Sea = false
local placeId = game.PlaceId
if placeId == 2753915549 then
First_Sea = true
elseif placeId == 4442272183 then
Second_Sea = true
elseif placeId == 7449423635 then
Third_Sea = true
end
--// Check Quest
function CheckLevel()
local Lv = game:GetService("Players").LocalPlayer.Data.Level.Value
if First_Sea then
if Lv == 1 or Lv <= 9 or SelectMonster == "Bandit" or SelectArea == '' then -- Bandit
Ms = "Bandit"
NameQuest = "BanditQuest1"
QuestLv = 1
NameMon = "Bandit"
CFrameQ = CFrame.new(1060.9383544922, 16.455066680908, 1547.7841796875)
CFrameMon = CFrame.new(1038.5533447266, 41.296249389648, 1576.5098876953)
elseif Lv == 10 or Lv <= 14 or SelectMonster == "Monkey" or SelectArea == 'Jungle' then -- Monkey
Ms = "Monkey"
NameQuest = "JungleQuest"
QuestLv = 1
NameMon = "Monkey"
CFrameQ = CFrame.new(-1601.6553955078, 36.85213470459, 153.38809204102)
CFrameMon = CFrame.new(-1448.1446533203, 50.851993560791, 63.60718536377)
elseif Lv == 15 or Lv <= 29 or SelectMonster == "Gorilla" or SelectArea == 'Jungle' then -- Gorilla
Ms = "Gorilla"
NameQuest = "JungleQuest"
QuestLv = 2
NameMon = "Gorilla"
CFrameQ = CFrame.new(-1601.6553955078, 36.85213470459, 153.38809204102)
CFrameMon = CFrame.new(-1142.6488037109, 40.462348937988, -515.39227294922)
Ms = "Pirate"
NameQuest = "BuggyQuest1"
QuestLv = 1
NameMon = "Pirate"
CFrameQ = CFrame.new(-1140.1761474609, 4.752049446106, 3827.4057617188)
CFrameMon = CFrame.new(-1201.0881347656, 40.628940582275, 3857.5966796875)
elseif Lv == 40 or Lv <= 59 or SelectMonster == "Brute" or SelectArea == 'Buggy' then -- Brute
Ms = "Brute"
NameQuest = "BuggyQuest1"
QuestLv = 2
NameMon = "Brute"
CFrameQ = CFrame.new(-1140.1761474609, 4.752049446106, 3827.4057617188)
CFrameMon = CFrame.new(-1387.5324707031, 24.592035293579, 4100.9575195313)
elseif Lv == 60 or Lv <= 74 or SelectMonster == "Desert Bandit" or SelectArea == 'Desert' then -- Desert Bandit
Ms = "Desert Bandit"
NameQuest = "DesertQuest"
QuestLv = 1
NameMon = "Desert Bandit"
CFrameQ = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
CFrameMon = CFrame.new(984.99896240234, 16.109552383423, 4417.91015625)
elseif Lv == 75 or Lv <= 89 or SelectMonster == "Desert Officer" or SelectArea == 'Desert' then -- Desert Officer
Ms = "Desert Officer"
NameQuest = "DesertQuest"
QuestLv = 2
NameMon = "Desert Officer"
CFrameQ = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
CFrameMon = CFrame.new(1547.1510009766, 14.452038764954, 4381.8002929688)
elseif Lv == 90 or Lv <= 99 or SelectMonster == "Snow Bandit" or SelectArea == 'Snow' then -- Snow Bandit
Ms = "Snow Bandit"
NameQuest = "SnowQuest"
QuestLv = 1
NameMon = "Snow Bandit"
CFrameQ = CFrame.new(1386.8073730469, 87.272789001465, -1298.3576660156)
CFrameMon = CFrame.new(1356.3028564453, 105.76865386963, -1328.2418212891)
elseif Lv == 100 or Lv <= 119 or SelectMonster == "Snowman" or SelectArea == 'Snow' then -- Snowman
Ms = "Snowman"
NameQuest = "SnowQuest"
QuestLv = 2
NameMon = "Snowman"
CFrameQ = CFrame.new(1386.8073730469, 87.272789001465, -1298.3576660156)
CFrameMon = CFrame.new(1218.7956542969, 138.01184082031, -1488.0262451172)
end
end
end

-------------------------------------------------------------------------------------------------------------------------------------------
---------Tween

  function Tween2(P1)
    local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance >= 1 then
    Speed = 300
    end
    game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear), {
      CFrame = P1
    }):Play()
    if _G.CancelTween2 then
    game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear), {
      CFrame = P1
    }):Cancel()
    end
    _G.Clip2 = true
    wait(Distance/Speed)
    _G.Clip2 = false
    end
   
-- [Function (Abandoned Quest , Others)]

function Com(com,...)
	local Remote = game:GetService('ReplicatedStorage').Remotes:FindFirstChild("Comm"..com)
	if Remote:IsA("RemoteEvent") then
		Remote:FireServer(...)
	elseif Remote:IsA("RemoteFunction") then
		Remote:InvokeServer(...)
	end
end

--BTP
function BTP(Position)
	game.Players.LocalPlayer.Character.Head:Destroy()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	wait(0.5)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
end
--BTPZ
function BTPZ(Point)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Point
    task.wait()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Point
        end
------Bypass TP 2
 function GetIsLand(...)
	local RealtargetPos = {...}
	local targetPos = RealtargetPos[1]
	local RealTarget
	if type(targetPos) == "vector" then
		RealTarget = targetPos
	elseif type(targetPos) == "userdata" then
		RealTarget = targetPos.Position
	elseif type(targetPos) == "number" then
		RealTarget = CFrame.new(unpack(RealtargetPos))
		RealTarget = RealTarget.p
	end

	local ReturnValue
	local CheckInOut = math.huge;
	if game.Players.LocalPlayer.Team then
		for i,v in pairs(game.Workspace._WorldOrigin.PlayerSpawns:FindFirstChild(tostring(game.Players.LocalPlayer.Team)):GetChildren()) do 
			local ReMagnitude = (RealTarget - v:GetModelCFrame().p).Magnitude;
			if ReMagnitude < CheckInOut then
				CheckInOut = ReMagnitude;
				ReturnValue = v.Name
			end
		end
		if ReturnValue then
			return ReturnValue
		end 
    end
end


     function toTarget(...)
    local RealtargetPos = { ... }
    local targetPos = RealtargetPos[1]
    local RealTarget
    if type(targetPos) == "vector" then
        RealTarget = CFrame.new(targetPos)
    elseif type(targetPos) == "userdata" then
        RealTarget = targetPos
    elseif type(targetPos) == "number" then
        RealTarget = CFrame.new(unpack(RealtargetPos))
    end
    if game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Health == 0 then
        if tween then tween:Cancel() end
        repeat wait(_G.Fast_Delay) until game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Health > 0; wait(0.2)
    end
    local tweenfunc = {}
    local Distance = (RealTarget.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position)
        .Magnitude
    if Distance < 1000 then
        Speed = 315
    elseif Distance >= 1000 then
        Speed = 300
    end
    if BypassTP then
        if Distance > 3000 and not AutoNextIsland and not (game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") or game.Players.LocalPlayer.Character:FindFirstChild("Special Microchip") or game.Players.LocalPlayer.Backpack:FindFirstChild("God's Chalice") or game.Players.LocalPlayer.Character:FindFirstChild("God's Chalice") or game.Players.LocalPlayer.Backpack:FindFirstChild("Hallow Essence") or game.Players.LocalPlayer.Character:FindFirstChild("Hallow Essence") or game.Players.LocalPlayer.Character:FindFirstChild("Sweet Chalice") or game.Players.LocalPlayer.Backpack:FindFirstChild("Sweet Chalice")) and not (Name == "Fishman Commando" or Name == "Fishman Warrior") then
            pcall(function()
                tween:Cancel()
                fkwarp = false
                if game:GetService("Players")["LocalPlayer"].Data:FindFirstChild("SpawnPoint").Value == tostring(GetIsLand(RealTarget)) then
                    wait(.1)
                    Com("F_", "TeleportToSpawn")
                elseif game:GetService("Players")["LocalPlayer"].Data:FindFirstChild("LastSpawnPoint").Value == tostring(GetIsLand(RealTarget)) then
                    game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid"):ChangeState(15)
                    wait(0.1)
                    repeat wait(_G.Fast_Delay) until game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0
                else
                    if game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                        if fkwarp == false then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = RealTarget
                        end
                        fkwarp = true
                    end
                    wait(.08)
                    game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid"):ChangeState(15)
                    repeat wait(_G.Fast_Delay) until game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0
                    wait(.1)
                    Com("F_", "SetSpawnPoint")
                end
                wait(0.2)

                return
            end)
        end
    end

    local tween_s = game:service "TweenService"
    local info = TweenInfo.new(
        (RealTarget.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position)
        .Magnitude / Speed, Enum.EasingStyle.Linear)
    local tweenw, err = pcall(function()
        tween = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, { CFrame = RealTarget })
        tween:Play()
    end)

    function tweenfunc:Stop()
        tween:Cancel()
    end

    function tweenfunc:Wait()
        tween.Completed:Wait()
    end

    return tweenfunc
end

----------------------------------------------------------------------------------------------------------------------------------------------
------AttackNoCD  
local plr = game.Players.LocalPlayer
local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))
local CbFw2 = CbFw[2]

function GetCurrentBlade() 
    local p13 = CbFw2.activeController
    local ret = p13.blades[1]
    if not ret then return end
    while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end
    return ret
end

function AttackNoCoolDown() 
    local AC = CbFw2.activeController
    for i = 1, 1 do 
        local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits(
            plr.Character,
            {plr.Character.HumanoidRootPart},
            60
        )
        local cac = {}
        local hash = {}
        for k, v in pairs(bladehit) do
            if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then
                table.insert(cac, v.Parent.HumanoidRootPart)
                hash[v.Parent] = true
            end
        end
        bladehit = cac
        if #bladehit > 0 then
            local u8 = debug.getupvalue(AC.attack, 5)
            local u9 = debug.getupvalue(AC.attack, 6)
            local u7 = debug.getupvalue(AC.attack, 4)
            local u10 = debug.getupvalue(AC.attack, 7)
            local u12 = (u8 * 798405 + u7 * 727595) % u9
            local u13 = u7 * 798405
            (function()
                u12 = (u12 * u9 + u13) % 1099511627776
                u8 = math.floor(u12 / u9)
                u7 = u12 - u8 * u9
            end)()
            u10 = u10 + 1
            debug.setupvalue(AC.attack, 5, u8)
            debug.setupvalue(AC.attack, 6, u9)
            debug.setupvalue(AC.attack, 4, u7)
            debug.setupvalue(AC.attack, 7, u10)
            pcall(function()
                for k, v in pairs(AC.animator.anims.basic) do
                    v:Play()
                end                  
            end)
            if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then 
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
                game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "") 
            end
        end
    end
end

-------------------------------------------------------------------------------------------------------------------------------------------
--Create Tabs
local Farm = Tabs.Main:AddSection("Farm")
local listfastattack = {'Normal Attack','Fast Attack','Super Fast Attack'}

    local DropdownDelayAttack = Tabs.Main:AddDropdown("DropdownDelayAttack", {
        Title = "Select Fast Attack",
        Description = "",
        Values = listfastattack,
        Multi = false,
        Default = 1,
    })
    DropdownDelayAttack:SetValue("Fast Attack")
    DropdownDelayAttack:OnChanged(function(Value)
    _G.FastAttackFaiFao_Mode = Value
	if _G.FastAttackFaiFao_Mode == "Fast Attack" then
		_G.Fast_Delay = 0.1
	elseif _G.FastAttackFaiFao_Mode == "Normal Attack" then
		_G.Fast_Delay = 0.2
	elseif _G.FastAttackFaiFao_Mode == "Super Fast Attack" then
		_G.Fast_Delay = 0
	end
end)

    local DropdownSelectWeapon = Tabs.Main:AddDropdown("DropdownSelectWeapon", {
        Title = "Weapon",
        Description = "Select Weapon",
        Values = {'Melee','Sword','Blox Fruit'},
        Multi = false,
        Default = 1,
    })
    DropdownSelectWeapon:SetValue('Melee')
    DropdownSelectWeapon:OnChanged(function(Value)
        ChooseWeapon = Value
    end)
    task.spawn(function()
        while wait() do
            pcall(function()
                if ChooseWeapon == "Melee" then
                    for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Melee" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                SelectWeapon = v.Name
                            end
                        end
                    end
                elseif ChooseWeapon == "Sword" then
                    for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Sword" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                SelectWeapon = v.Name
                            end
                        end
                    end
                elseif ChooseWeapon == "Blox Fruit" then
                    for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Blox Fruit" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                SelectWeapon = v.Name
                            end
                        end
                    end
                else
                    for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Melee" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                SelectWeapon = v.Name
                            end
                        end
                    end
                end
            end)
        end
    end)


    local ToggleLevel = Tabs.Main:AddToggle("ToggleLevel", {
        Title = "Auto Farm",
        Description = "",
        Default = false })
    ToggleLevel:OnChanged(function(Value)
        _G.AutoLevel = Value
        if Value == false then
            wait()
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            wait()
        end
    end)
    Options.ToggleLevel:SetValue(false)
    spawn(function()
        while task.wait() do
        if _G.AutoLevel then
        pcall(function()
          CheckLevel()
          if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
          game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
          toTarget(CFrameQ)
          if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
          game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
          end
          elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
          for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
          if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
          if v.Name == Ms then
          repeat wait(_G.Fast_Delay)
          AttackNoCoolDown()
          bringmob = true
          AutoHaki()
          EquipTool(SelectWeapon)
          Tween(v.HumanoidRootPart.CFrame * CFrame.new(posX,posY,posZ))
          v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
          v.HumanoidRootPart.Transparency = 1
          v.Humanoid.JumpPower = 0
          v.Humanoid.WalkSpeed = 0
          v.HumanoidRootPart.CanCollide = false
          FarmPos = v.HumanoidRootPart.CFrame
          MonFarm = v.Name
          until not _G.AutoLevel or not v.Parent or v.Humanoid.Health <= 0 or not game:GetService("Workspace").Enemies:FindFirstChild(v.Name) or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
          bringmob = false
        end   
          end
          end
          for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].EnemySpawns:GetChildren()) do
          if string.find(v.Name,NameMon) then
          if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude >= 10 then
            Tween(v.CFrame * CFrame.new(posX,posY,posZ))
          end
          end
          end
          end
          end)
        end
        end
        end)
        
        
        
        
        local ToggleMelee = Tabs.Stats:AddToggle("ToggleMelee", {Title = "Auto Melee",Description = "Up Melee", Default = false })
ToggleMelee:OnChanged(function(Value)
    _G.Auto_Stats_Melee = Value
    end)
Options.ToggleMelee:SetValue(false)



local ToggleDe = Tabs.Stats:AddToggle("ToggleDe", {Title = "Auto Defense",Description = "UpDefense", Default = false })
ToggleDe:OnChanged(function(Value)
    _G.Auto_Stats_Defense = Value
    end)
Options.ToggleDe:SetValue(false)



local ToggleSword = Tabs.Stats:AddToggle("ToggleSword", {Title = "Auto Sword",Description = "Up Sword", Default = false })
ToggleSword:OnChanged(function(Value)
    _G.Auto_Stats_Sword = Value
    end)
Options.ToggleSword:SetValue(false)



local ToggleGun = Tabs.Stats:AddToggle("ToggleGun", {Title = "Auto Gun", Description = "Up Gun",Default = false })
ToggleGun:OnChanged(function(Value)
    _G.Auto_Stats_Gun = Value
    end)
Options.ToggleGun:SetValue(false)


local ToggleFruit = Tabs.Stats:AddToggle("ToggleFruit", {Title = "Auto Fruit",Description = "Up Fruit", Default = false })
ToggleFruit:OnChanged(function(Value)
    _G.Auto_Stats_Devil_Fruit = Value
    end)
Options.ToggleFruit:SetValue(false)


spawn(function()
    while wait() do
        if _G.Auto_Stats_Devil_Fruit then
            local args = {
                [1] = "AddPoint",
                [2] = "Demon Fruit",
                [3] = 3
            }
                        
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    end
end)

spawn(function()
    while wait() do
        if _G.Auto_Stats_Gun then
            local args = {
                [1] = "AddPoint",
                [2] = "Gun",
                [3] = 3
            }
                        
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    end
end)


spawn(function()
    while wait() do
        if _G.Auto_Stats_Sword then
            local args = {
                [1] = "AddPoint",
                [2] = "Sword",
                [3] = 3
            }
                        
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    end
end)

spawn(function()
    while wait() do
        if _G.Auto_Stats_Defense then
            local args = {
                [1] = "AddPoint",
                [2] = "Defense",
                [3] = 3
            }
                        
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    end
end)


spawn(function()
    while wait() do
        if _G.Auto_Stats_Melee then
            local args = {
                [1] = "AddPoint",
                [2] = "Melee",
                [3] = 3
            }
                        
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    end
end)

SaveManager:IgnoreThemeSettings()

InterfaceManager:SetFolder("FluentScriptHub")
SaveManager:SetFolder("FluentScriptHub/specific-game")

InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)


Window:SelectTab(1)

Fluent:Notify({
    Title = "Maruko Hub",
    Content = "The script has been loaded.",
    Duration = 8
})

SaveManager:LoadAutoloadConfig()