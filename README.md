----Hub Pedroxz Troll, Sei que copiar mais nao adianta baby----
----Entrou aqui se ferrou! Pq ja to com acesso do seu pc hahaha----
local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/cueshut/saves/main/criminality%20paste%20ui%20library'))()

-- // Window \\ --
local window = library.new('Pedroxz Menu Troll', 'leadmarker')

-- // Tabs \\ --
local tab = window.new_tab('rbxassetid://4483345998')
local tab1 = window.new_tab('rbxassetid://4483345998')

-- // Sections \\ --
local section =  tab.new_section('Jogadores')
local section1 = tab.new_section('Players')

-- // Sector \\ --
local sector = section.new_sector('Jogador', 'Left')
local sector1 = section.new_sector('Cheats', 'Right')

-- // Elements \\ -- (Type, Name, State, Callback)
local button = sector.element('Button', 'Anti ADM V2', nil, function()
end)
   local button = sector.element('Button', 'GodMode', nil, function()
      local Player = game.Players.LocalPlayer
      local Character = Player.Character
      local Humanoid = Character.Humanoid
       
      print('Godmode working.')
       
      Humanoid.MaxHealth = 999999
      Humanoid.Health = Humanoid.MaxHealth / 2
       
      Humanoid.HealthChanged:connect(function()
          if Humanoid.Health < 10 then
              Humanoid.Health = Humanoid.MaxHealth
          end
      end)
end)

local toggle = sector.element('Toggle', 'Aimbot', false, function(v)
   loadstring(game:HttpGet(('https://raw.githubusercontent.com/Exunys/Aimbot-V2/main/Resources/Scripts/Main.lua'),true))()
end)
local toggle = sector.element('Toggle', 'Fly', false, function(v)
   loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\103\105\115\116\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\109\101\111\122\111\110\101\89\84\47\98\102\48\51\55\100\102\102\57\102\48\97\55\48\48\49\55\51\48\52\100\100\100\54\55\102\100\99\100\51\55\48\47\114\97\119\47\101\49\52\101\55\52\102\52\50\53\98\48\54\48\100\102\53\50\51\51\52\51\99\102\51\48\98\55\56\55\48\55\52\101\98\51\99\53\100\50\47\97\114\99\101\117\115\37\50\53\50\48\120\37\50\53\50\48\102\108\121\37\50\53\50\48\50\37\50\53\50\48\111\98\102\108\117\99\97\116\111\114\39\41\44\116\114\117\101\41\41\40\41\10\10")()
end)
local toggle = sector.element('Toggle', 'Puxar Geral', false, function(v)
   loadstring(game:HttpGet(("https://raw.githubusercontent.com/GameLeaks2/RobloxScripts/main/BRING%20ALL%20-%20EB'S"),true))()
end)
local button = sector1.element('Button', 'Banir Geral', nil, function()
   
end)
local button = sector1.element('Button', 'Tp Player', nil, function()
   local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Pedroxz Teleport", "DarkTheme")
local Tab = Window:NewTab("Players")
local Section = Tab:NewSection("Teleport")
 
--------------------
 
players = {}
 
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
 
Section:NewDropdown("Select Player", " ", players, function(abc)
    Select = abc
end)
 
 
Section:NewButton("Refresh", " ", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
end)
 
Section:NewButton("Teleport", " ", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame
end)
end)
local toggle = sector.element('Toggle', 'Ficar Invisivel', false, function(v)
   local ScriptStarted = false
   local Keybind = "E" --Set to whatever you want, has to be the name of a KeyCode Enum.
   local Transparency = true --Will make you slightly transparent when you are invisible. No reason to disable.
   local NoClip = false --Will make your fake character no clip.
   local Player = game:GetService("Players").LocalPlayer
   local RealCharacter = Player.Character or Player.CharacterAdded:Wait()
   local IsInvisible = false
   RealCharacter.Archivable = true
   local FakeCharacter = RealCharacter:Clone()
   local Part
   Part = Instance.new("Part", workspace)
   Part.Anchored = true
   Part.Size = Vector3.new(200, 1, 200)
   Part.CFrame = CFrame.new(0, -500, 0) --Set this to whatever you want, just far away from the map.
   Part.CanCollide = true
   FakeCharacter.Parent = workspace
   FakeCharacter.HumanoidRootPart.CFrame = Part.CFrame * CFrame.new(0, 5, 0)
   for i, v in pairs(RealCharacter:GetChildren()) do
     if v:IsA("LocalScript") then
         local clone = v:Clone()
         clone.Disabled = true
         clone.Parent = FakeCharacter
     end
   end
   if Transparency then
     for i, v in pairs(FakeCharacter:GetDescendants()) do
         if v:IsA("BasePart") then
             v.Transparency = 0.7
         end
     end
   end
   local CanInvis = true
   function RealCharacterDied()
     CanInvis = false
     RealCharacter:Destroy()
     RealCharacter = Player.Character
     CanInvis = true
     isinvisible = false
     FakeCharacter:Destroy()
     workspace.CurrentCamera.CameraSubject = RealCharacter.Humanoid
     RealCharacter.Archivable = true
     FakeCharacter = RealCharacter:Clone()
     Part:Destroy()
     Part = Instance.new("Part", workspace)
     Part.Anchored = true
     Part.Size = Vector3.new(200, 1, 200)
     Part.CFrame = CFrame.new(9999, 9999, 9999) --Set this to whatever you want, just far away from the map.
     Part.CanCollide = true
     FakeCharacter.Parent = workspace
     FakeCharacter.HumanoidRootPart.CFrame = Part.CFrame * CFrame.new(0, 5, 0)
     for i, v in pairs(RealCharacter:GetChildren()) do
         if v:IsA("LocalScript") then
             local clone = v:Clone()
             clone.Disabled = true
             clone.Parent = FakeCharacter
         end
     end
     if Transparency then
         for i, v in pairs(FakeCharacter:GetDescendants()) do
             if v:IsA("BasePart") then
                 v.Transparency = 0.7
             end
         end
     end
    RealCharacter.Humanoid.Died:Connect(function()
    RealCharacter:Destroy()
    FakeCharacter:Destroy()
    end)
    Player.CharacterAppearanceLoaded:Connect(RealCharacterDied)
   end
   RealCharacter.Humanoid.Died:Connect(function()
    RealCharacter:Destroy()
    FakeCharacter:Destroy()
    end)
   Player.CharacterAppearanceLoaded:Connect(RealCharacterDied)
   local PseudoAnchor
   game:GetService "RunService".RenderStepped:Connect(
     function()
         if PseudoAnchor ~= nil then
             PseudoAnchor.CFrame = Part.CFrame * CFrame.new(0, 5, 0)
         end
          if NoClip then
         FakeCharacter.Humanoid:ChangeState(11)
          end
     end
   )
   PseudoAnchor = FakeCharacter.HumanoidRootPart
   local function Invisible()
     if IsInvisible == false then
         local StoredCF = RealCharacter.HumanoidRootPart.CFrame
         RealCharacter.HumanoidRootPart.CFrame = FakeCharacter.HumanoidRootPart.CFrame
         FakeCharacter.HumanoidRootPart.CFrame = StoredCF
         RealCharacter.Humanoid:UnequipTools()
         Player.Character = FakeCharacter
         workspace.CurrentCamera.CameraSubject = FakeCharacter.Humanoid
         PseudoAnchor = RealCharacter.HumanoidRootPart
         for i, v in pairs(FakeCharacter:GetChildren()) do
             if v:IsA("LocalScript") then
                 v.Disabled = false
             end
         end
         IsInvisible = true
     else
         local StoredCF = FakeCharacter.HumanoidRootPart.CFrame
         FakeCharacter.HumanoidRootPart.CFrame = RealCharacter.HumanoidRootPart.CFrame
    
         RealCharacter.HumanoidRootPart.CFrame = StoredCF
    
         FakeCharacter.Humanoid:UnequipTools()
         Player.Character = RealCharacter
         workspace.CurrentCamera.CameraSubject = RealCharacter.Humanoid
         PseudoAnchor = FakeCharacter.HumanoidRootPart
         for i, v in pairs(FakeCharacter:GetChildren()) do
             if v:IsA("LocalScript") then
                 v.Disabled = true
             end
         end
         IsInvisible = false
     end
   end
   game:GetService("UserInputService").InputBegan:Connect(
     function(key, gamep)
         if gamep then
             return
         end
         if key.KeyCode.Name:lower() == Keybind:lower() and CanInvis and RealCharacter and FakeCharacter then
             if RealCharacter:FindFirstChild("HumanoidRootPart") and FakeCharacter:FindFirstChild("HumanoidRootPart") then
                 Invisible()
             end
         end
     end
   )
   local Sound = Instance.new("Sound",game:GetService("SoundService"))
   Sound.SoundId = "rbxassetid://232127604"
   Sound:Play()
   game:GetService("StarterGui"):SetCore("SendNotification",{["Title"] = "Invisivel Carregado!",["Text"] = "Pressione "..Keybind.." Para usar o invisivel!",["Duration"] = 20,["Button1"] = "Okay."})
end)
local toggle = sector.element('Toggle', 'Puxar Armas V9', false, function(v)
   for i, v in pairs(game:GetDescendants()) do
      if v:IsA('Tool') then
          v.Parent = game:GetService('Players').LocalPlayer.Backpack
      end
  end
  
  game:GetService('Players').LocalPlayer.Character.Humanoid.Died:Connect(function()
      for i, v in pairs(game:GetService('Players').LocalPlayer.Backpack:GetDescendants()) do
          if v:IsA('Tool') then
              v.Parent = game:GetService('Teams')
          end
      end
      for i, v in pairs(game:GetService('Players').LocalPlayer.Character:GetDescendants()) do
          if v:IsA('Tool') then
              v.Parent = game:GetService('Teams')
          end
      end
  end)
end)
toggle:add_color({Color = Color3.fromRGB(84, 101, 255)}, nil, function(v)
   print(v.Color)    
end)

local dropdown = sector.element('Dropdown', 'Players', {options = {'one', 'two', 'three'}}, function(v)
   print(v.Dropdown)
end)

local slider = sector.element('Slider', 'Speed', {default = {min = 16, max = 5000, default = 16}}, function(v)
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
end)

local combo = sector.element('Combo', 'Explodir Geral', {options = {'players', 'all'}}, function(v)
   local rem,_t,players = game:GetService("ReplicatedStorage").ACS_Engine.Eventos.Hit,{ExplosiveHit=true,ExPressure=math.huge,ExpRadius=math.huge,DestroyJointRadiusPercent=math.huge,ExplosionDamage=math.huge},game:GetService('Players')
	
   for i,v in next, players:GetPlayers() do 
      local ppart = v['Character'].PrimaryPart
      pcall(function()
         rem:FireServer(ppart.Position,ppart,ppart.Position,Enum.Material.ForceField,_t)
      end)
   end
end)
