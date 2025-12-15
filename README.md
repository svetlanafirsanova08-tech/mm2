local player = game.Players.LocalPlayer 
local CoreGui = game:GetService("CoreGui")
 local roles = ""
local Noclip = Instance.new("ScreenGui")
local BG2 = Instance.new("Frame")
local BG = Instance.new("ScrollingFrame")
local tpscrolingframe = Instance.new("ScrollingFrame")
local hitbox = Instance.new("TextButton")
local MoneyHave = Instance.new("TextLabel")
local killAll = Instance.new("TextButton")
local StartFarm = Instance.new("TextButton")
local farmScrolingFrame = Instance.new("ScrollingFrame") -- Будующий автофарм СДЕЛАТЬ
local buttonFarm = Instance.new("TextButton")
local farmwork = false 
local Title = Instance.new("TextLabel")
local Titlsheriff = Instance.new("TextLabel")
local BotsTitle = Instance.new("TextLabel")
local Titltptoperson = Instance.new("TextLabel")
local Title2player = Instance.new("TextLabel")
local Titleteleport = Instance.new("TextLabel")
local FarmTitle = Instance.new("TextLabel")
local Titletpforfindperson= Instance.new("TextLabel")
local playerbutton = Instance.new("TextButton")
local rolesbutton = Instance.new("TextButton")
local teleportbutton = Instance.new("TextButton")
local gundropwork = false
local murkillwork = false
local gundropclaim = Instance.new("TextButton")
local resetifmes = Instance.new("TextButton")
local murkill = Instance.new("TextButton")
local printifautofarmstopped = Instance.new("TextButton")
local jump = Instance.new("TextButton")
local jumpBox = Instance.new("TextBox")
local noclip = Instance.new("TextButton")
local antifling = Instance.new("TextButton")
local tptomardered = Instance.new("TextButton")
local tptoshriff = Instance.new("TextButton")
local mirkillcan = true 
local exp = Instance.new("TextButton")
local  noclip  = Instance.new("TextButton")
local noclipwork = false
local expwork = false
local  playerFrame = Instance.new("ScrollingFrame")
local  teleportFrame = Instance.new("ScrollingFrame")
local speed = Instance.new("TextButton")
local speedBox = Instance.new("TextBox")
local teleportLobby = Instance.new("TextButton")
local teleportMap = Instance.new("TextButton")
local playertp1 = Instance.new("TextButton")
local playertp2 = Instance.new("TextButton")
local playertp3 = Instance.new("TextButton")
local playertp4 = Instance.new("TextButton")
local playertp5 = Instance.new("TextButton")
local playertp6 = Instance.new("TextButton")
local playertp7 = Instance.new("TextButton")
local playertp8 = Instance.new("TextButton")
local playertp9 = Instance.new("TextButton")
local playertp10 = Instance.new("TextButton")
local playertp11 = Instance.new("TextButton")
local xray = Instance.new("TextButton")
local twins = game:GetService("TweenService")
local folder = ""
local targetcoin = ""
local coin2 = nil
local posmin = 999999999
local animationSettings = TweenInfo.new(0.1, Enum.EasingStyle.Linear)
local farmwork = false
local farmEnable = false
local mes = false 
local mescan = false
local VirtualUser = game:GetService("VirtualUser")
local killifmesenge = false 

local xraywork = false 

		local Players = game:GetService("Players")
local VirtualInputManager = game:GetService("VirtualInputManager")
local player = Players.LocalPlayer
local mouse = player:GetMouse()

-- Способ 1: Через позицию мыши
function clickMouse()
    local x, y = mouse.X, mouse.Y
    VirtualInputManager:SendMouseButtonEvent(x, y, 0, true, game, false)
    wait(0.05)
    VirtualInputManager:SendMouseButtonEvent(x, y, 0, false, game, false)
end

local speedwork = false

local jumpwork = false
local hitbox100 = false
local canKillAll = true 

Noclip.Name = "autofarmmoney"
Noclip.Parent = game.CoreGui

BG2.Name = "BG2"
BG2.Parent = Noclip
BG2.BackgroundColor3 = Color3.new(0.0980392, 0.0980392, 0.0980392)
BG2.BorderColor3 = Color3.new(0.0588235, 0.0588235, 0.0588235)
BG2.BorderSizePixel = 2
BG2.Position = UDim2.new(0.149479166, 0, 0.9, 0)
BG2.Size = UDim2.new(0, 550, 0, 450)
BG2.Active = true
BG2.Draggable = true 

BG.Name = "BG"
BG.Parent = BG2
BG.BackgroundColor3 = Color3.new(0.0980392, 0.0980392, 0.0980392)
BG.BorderColor3 = Color3.new(0.0588235, 0.0588235, 0.0588235)
BG.BorderSizePixel = 2
BG.Position = UDim2.new(0, 50, 0, 50)
BG.Size = UDim2.new(0, 500, 0, 400)
BG.Active = true


tpscrolingframe.Name = "tp"
tpscrolingframe.Parent = teleportFrame
tpscrolingframe.BackgroundColor3 = Color3.new(0.0980392, 0.0980392, 0.0980392)
tpscrolingframe.BorderColor3 = Color3.new(0.0588235, 0.0588235, 0.0588235)
tpscrolingframe.BorderSizePixel = 2
tpscrolingframe.Position = UDim2.new(0, 150, 0, 300)
tpscrolingframe.Size = UDim2.new(0, 200, 0, 200)
tpscrolingframe.Active = true




teleportFrame.Name = "playerFrame"
teleportFrame.Visible = false
teleportFrame.Parent = BG2
teleportFrame.BackgroundColor3 = Color3.new(0.0980392, 0.0980392, 0.0980392)
teleportFrame.BorderColor3 = Color3.new(0.0588235, 0.0588235, 0.0588235)
teleportFrame.BorderSizePixel = 2
teleportFrame.Position = UDim2.new(0, 50, 0, 50)
teleportFrame.Size = UDim2.new(0, 500, 0, 400)
teleportFrame.Active = true


farmScrolingFrame.Name = "playerFrame"
farmScrolingFrame.Visible = false
farmScrolingFrame.Parent = BG2
farmScrolingFrame.BackgroundColor3 = Color3.new(0.0980392, 0.0980392, 0.0980392)
farmScrolingFrame.BorderColor3 = Color3.new(0.0588235, 0.0588235, 0.0588235)
farmScrolingFrame.BorderSizePixel = 2
farmScrolingFrame.Position = UDim2.new(0, 50, 0, 50)
farmScrolingFrame.Size = UDim2.new(0, 500, 0, 400)
farmScrolingFrame.Active = true


playerFrame.Name = "playerFrame"
playerFrame.Visible = false
playerFrame.Parent = BG2
playerFrame.BackgroundColor3 = Color3.new(0.0980392, 0.0980392, 0.0980392)
playerFrame.BorderColor3 = Color3.new(0.0588235, 0.0588235, 0.0588235)
playerFrame.BorderSizePixel = 2
playerFrame.Position = UDim2.new(0, 50, 0, 50)
playerFrame.Size = UDim2.new(0, 500, 0, 400)
playerFrame.Active = true

rolesbutton.Parent = BG2
rolesbutton.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
rolesbutton.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
rolesbutton.BorderSizePixel = 2
rolesbutton.Position = UDim2.new(0, 0, 0, 100)
rolesbutton.Size = UDim2.new(0, 45, 0, 45)
rolesbutton.Font = Enum.Font.Highway
rolesbutton.FontSize = Enum.FontSize.Size28
rolesbutton.Text = "roles"
rolesbutton.TextColor3 = Color3.new(1, 1, 1)
rolesbutton.TextSize = 15
rolesbutton.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
rolesbutton.TextStrokeTransparency = 0


teleportbutton.Parent = BG2
teleportbutton.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
teleportbutton.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
teleportbutton.BorderSizePixel = 2
teleportbutton.Position = UDim2.new(0, 0, 0, 150)
teleportbutton.Size = UDim2.new(0, 45, 0, 45)
teleportbutton.Font = Enum.Font.Highway
teleportbutton.FontSize = Enum.FontSize.Size28
teleportbutton.Text = "teleport"
teleportbutton.TextColor3 = Color3.new(1, 1, 1)
teleportbutton.TextSize = 15
teleportbutton.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
teleportbutton.TextStrokeTransparency = 0






playerbutton.Parent = BG2
playerbutton.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playerbutton.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playerbutton.BorderSizePixel = 2
playerbutton.Position = UDim2.new(0, 0, 0, 50)
playerbutton.Size = UDim2.new(0, 45, 0, 45)
playerbutton.Font = Enum.Font.Highway
playerbutton.FontSize = Enum.FontSize.Size28
playerbutton.Text = "player"
playerbutton.TextColor3 = Color3.new(1, 1, 1)
playerbutton.TextSize = 15
playerbutton.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playerbutton.TextStrokeTransparency = 0

buttonFarm.Parent = BG2
buttonFarm.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
buttonFarm.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
buttonFarm.BorderSizePixel = 2
buttonFarm.Position = UDim2.new(0, 0, 0, 200)
buttonFarm.Size = UDim2.new(0, 45, 0, 45)
buttonFarm.Font = Enum.Font.Highway
buttonFarm.FontSize = Enum.FontSize.Size28
buttonFarm.Text = "farm"
buttonFarm.TextColor3 = Color3.new(1, 1, 1)
buttonFarm.TextSize = 15
buttonFarm.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
buttonFarm.TextStrokeTransparency = 0

Title2player.Name = "Title"
Title2player.Parent = playerFrame
Title2player.BackgroundTransparency = 1
Title2player.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
Title2player.BorderSizePixel = 2
Title2player.Size = UDim2.new(0, 300, 0, 33)
Title2player.Font = Enum.Font.Highway
Title2player.Text = "player "
Title2player.TextColor3 = Color3.new(1, 1, 1)
Title2player.FontSize = Enum.FontSize.Size32
Title2player.TextSize = 30
Title2player.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
Title2player.TextStrokeTransparency = 0
Title2player.Position = UDim2.new(0.159980958, 0, 0.014192119, 0)

Titleteleport.Name = "Title"
Titleteleport.Parent = teleportFrame
Titleteleport.BackgroundTransparency = 1
Titleteleport.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
Titleteleport.BorderSizePixel = 2
Titleteleport.Size = UDim2.new(0, 300, 0, 33)
Titleteleport.Font = Enum.Font.Highway
Titleteleport.Text = "teleport to location "
Titleteleport.TextColor3 = Color3.new(1, 1, 1)
Titleteleport.FontSize = Enum.FontSize.Size32
Titleteleport.TextSize = 30
Titleteleport.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
Titleteleport.TextStrokeTransparency = 0
Titleteleport.Position = UDim2.new(0.159980958, 0, 0.014192119, 0)


FarmTitle.Name = "Title"
FarmTitle.Parent = farmScrolingFrame 
FarmTitle.BackgroundTransparency = 1
FarmTitle.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
FarmTitle.BorderSizePixel = 2
FarmTitle.Size = UDim2.new(0, 300, 0, 33)
FarmTitle.Font = Enum.Font.Highway
FarmTitle.Text = "AutoFarm(player)"
FarmTitle.TextColor3 = Color3.new(1, 1, 1)
FarmTitle.FontSize = Enum.FontSize.Size32
FarmTitle.TextSize = 30
FarmTitle.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
FarmTitle.TextStrokeTransparency = 0
FarmTitle.Position = UDim2.new(0.159980958, 0, 0.014192119, 0)


Titlsheriff.Name = "Title"
Titlsheriff.Parent = BG
Titlsheriff.BackgroundTransparency = 1
Titlsheriff.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
Titlsheriff.BorderSizePixel = 2
Titlsheriff.Size = UDim2.new(0, 300, 0, 33)
Titlsheriff.Font = Enum.Font.Highway
Titlsheriff.Text = "Sheriff function "
Titlsheriff.TextColor3 = Color3.new(1, 1, 1)
Titlsheriff.FontSize = Enum.FontSize.Size32
Titlsheriff.TextSize = 30
Titlsheriff.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
Titlsheriff.TextStrokeTransparency = 0
Titlsheriff.Position = UDim2.new(0.179980958, 0, 0.151192119, 0)


BotsTitle .Name = "Title"
BotsTitle .Parent = farmScrolingFrame
BotsTitle .BackgroundTransparency = 1
BotsTitle .BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
BotsTitle .BorderSizePixel = 2
BotsTitle .Size = UDim2.new(0, 300, 0, 33)
BotsTitle .Font = Enum.Font.Highway
BotsTitle .Text = "Bots function "
BotsTitle .TextColor3 = Color3.new(1, 1, 1)
BotsTitle .FontSize = Enum.FontSize.Size32
BotsTitle .TextSize = 30
BotsTitle .TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
BotsTitle .TextStrokeTransparency = 0
BotsTitle .Position = UDim2.new(0.179980958, 0, 0.151192119, 0)


Titltptoperson.Name = "Title"
Titltptoperson.Parent = teleportFrame
Titltptoperson.BackgroundTransparency = 1
Titltptoperson.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
Titltptoperson.BorderSizePixel = 2
Titltptoperson.Size = UDim2.new(0, 300, 0, 33)
Titltptoperson.Font = Enum.Font.Highway
Titltptoperson.Text = "teleport to person"
Titltptoperson.TextColor3 = Color3.new(1, 1, 1)
Titltptoperson.FontSize = Enum.FontSize.Size32
Titltptoperson.TextSize = 30
Titltptoperson.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
Titltptoperson.TextStrokeTransparency = 0
Titltptoperson.Position = UDim2.new(0.179980958, 0, 0.151192119, 0)

Titletpforfindperson.Name = "Title"
Titletpforfindperson.Parent = teleportFrame
Titletpforfindperson.BackgroundTransparency = 1
Titletpforfindperson.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
Titletpforfindperson.BorderSizePixel = 2
Titletpforfindperson.Size = UDim2.new(0, 300, 0, 33)
Titletpforfindperson.Font = Enum.Font.Highway
Titletpforfindperson.Text = "teleport to certain player"
Titletpforfindperson.TextColor3 = Color3.new(1, 1, 1)
Titletpforfindperson.FontSize = Enum.FontSize.Size32
Titletpforfindperson.TextSize = 30
Titletpforfindperson.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
Titletpforfindperson.TextStrokeTransparency = 0
Titletpforfindperson.Position = UDim2.new(0.179980958, 0, 0.281192119, 0)




Title.Name = "Title"
Title.Parent = BG
Title.BackgroundTransparency = 1
Title.BorderColor3 = Color3.new(0.192157, 0.352941, 0.0235294)
Title.BorderSizePixel = 2
Title.Size = UDim2.new(0, 300, 0, 33)
Title.Font = Enum.Font.Highway
Title.Text = "Murder function "
Title.TextColor3 = Color3.new(1, 1, 1)
Title.FontSize = Enum.FontSize.Size32
Title.TextSize = 30
Title.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
Title.TextStrokeTransparency = 0
Title.Position = UDim2.new(0.159980958, 0, 0.014192119, 0)


murkill.Parent = BG
murkill.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
murkill.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
murkill.BorderSizePixel = 2
murkill.Position = UDim2.new(0.022380958, 0, 0.20192119, 0)
murkill.Size = UDim2.new(0, 200, 0, 60)
murkill.Font = Enum.Font.Highway
murkill.FontSize = Enum.FontSize.Size28
murkill.Text = "Killmurder"
murkill.TextColor3 = Color3.new(1, 1, 1)
murkill.TextSize = 25
murkill.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
murkill.TextStrokeTransparency = 0




printifautofarmstopped.Parent = farmScrolingFrame
printifautofarmstopped.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
printifautofarmstopped.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
printifautofarmstopped.BorderSizePixel = 2
printifautofarmstopped.Position = UDim2.new(0.022380958, 0, 0.20192119, 0)
printifautofarmstopped.Size = UDim2.new(0, 200, 0, 60)
printifautofarmstopped.Font = Enum.Font.Highway
printifautofarmstopped.FontSize = Enum.FontSize.Size28
printifautofarmstopped.Text = "Print OFF"
printifautofarmstopped.TextColor3 = Color3.new(1, 1, 1)
printifautofarmstopped.TextSize = 25
printifautofarmstopped.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
printifautofarmstopped.TextStrokeTransparency = 0



tptomardered.Parent = teleportFrame
tptomardered.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
tptomardered.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
tptomardered.BorderSizePixel = 2
tptomardered.Position = UDim2.new(0.022380958, 0, 0.20192119, 0)
tptomardered.Size = UDim2.new(0, 200, 0, 60)
tptomardered.Font = Enum.Font.Highway
tptomardered.FontSize = Enum.FontSize.Size28
tptomardered.Text = "murdered"
tptomardered.TextColor3 = Color3.new(1, 1, 1)
tptomardered.TextSize = 25
tptomardered.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
tptomardered.TextStrokeTransparency = 0


gundropclaim.Parent = BG
gundropclaim.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
gundropclaim.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
gundropclaim.BorderSizePixel = 2
gundropclaim.Position = UDim2.new(0.52380958, 0, 0.20192119, 0)
gundropclaim.Size = UDim2.new(0, 200, 0, 60)
gundropclaim.Font = Enum.Font.Highway
gundropclaim.FontSize = Enum.FontSize.Size28
gundropclaim.Text = "GunAutoClaim OFF"
gundropclaim.TextColor3 = Color3.new(1, 1, 1)
gundropclaim.TextSize = 25
gundropclaim.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
gundropclaim.TextStrokeTransparency = 0


resetifmes .Parent = farmScrolingFrame
resetifmes .BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
resetifmes .BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
resetifmes .BorderSizePixel = 2
resetifmes .Position = UDim2.new(0.52380958, 0, 0.20192119, 0)
resetifmes .Size = UDim2.new(0, 200, 0, 60)
resetifmes .Font = Enum.Font.Highway
resetifmes .FontSize = Enum.FontSize.Size28
resetifmes .Text = "kill if print OFF"
resetifmes .TextColor3 = Color3.new(1, 1, 1)
resetifmes .TextSize = 25
resetifmes .TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
resetifmes .TextStrokeTransparency = 0



playertp1.Parent = tpscrolingframe
playertp1.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp1.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp1.BorderSizePixel = 2
playertp1.Position = UDim2.new(0, 0, 0, 0)
playertp1.Size = UDim2.new(0, 200, 0, 60)
playertp1.Font = Enum.Font.Highway
playertp1.FontSize = Enum.FontSize.Size28
playertp1.Text = "no player"
playertp1.TextColor3 = Color3.new(1, 1, 1)
playertp1.TextSize = 25
playertp1.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp1.TextStrokeTransparency = 0


playertp2.Parent = tpscrolingframe
playertp2.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp2.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp2.BorderSizePixel = 2
playertp2.Position = UDim2.new(0, 0, 0.08, 0)
playertp2.Size = UDim2.new(0, 200, 0, 60)
playertp2.Font = Enum.Font.Highway
playertp2.FontSize = Enum.FontSize.Size28
playertp2.Text = "no player"
playertp2.TextColor3 = Color3.new(1, 1, 1)
playertp2.TextSize = 25
playertp2.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp2.TextStrokeTransparency = 0

playertp3.Parent = tpscrolingframe
playertp3.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp3.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp3.BorderSizePixel = 2
playertp3.Position = UDim2.new(0, 0, 0.16, 0)
playertp3.Size = UDim2.new(0, 200, 0, 60)
playertp3.Font = Enum.Font.Highway
playertp3.FontSize = Enum.FontSize.Size28
playertp3.Text = "no player"
playertp3.TextColor3 = Color3.new(1, 1, 1)
playertp3.TextSize = 25
playertp3.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp3.TextStrokeTransparency = 0

playertp4.Parent = tpscrolingframe
playertp4.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp4.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp4.BorderSizePixel = 2
playertp4.Position = UDim2.new(0, 0, 0.24, 0)
playertp4.Size = UDim2.new(0, 200, 0, 60)
playertp4.Font = Enum.Font.Highway
playertp4.FontSize = Enum.FontSize.Size28
playertp4.Text = "no player"
playertp4.TextColor3 = Color3.new(1, 1, 1)
playertp4.TextSize = 25
playertp4.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp4.TextStrokeTransparency = 0


playertp5.Parent = tpscrolingframe
playertp5.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp5.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp5.BorderSizePixel = 2
playertp5.Position = UDim2.new(0, 0, 0.32, 0)
playertp5.Size = UDim2.new(0, 200, 0, 60)
playertp5.Font = Enum.Font.Highway
playertp5.FontSize = Enum.FontSize.Size28
playertp5.Text = "no player"
playertp5.TextColor3 = Color3.new(1, 1, 1)
playertp5.TextSize = 25
playertp5.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp5.TextStrokeTransparency = 0


playertp6.Parent = tpscrolingframe
playertp6.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp6.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp6.BorderSizePixel = 2
playertp6.Position = UDim2.new(0, 0, 0.40, 0)
playertp6.Size = UDim2.new(0, 200, 0, 60)
playertp6.Font = Enum.Font.Highway
playertp6.FontSize = Enum.FontSize.Size28
playertp6.Text = "no player"
playertp6.TextColor3 = Color3.new(1, 1, 1)
playertp6.TextSize = 25
playertp6.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp6.TextStrokeTransparency = 0


playertp7.Parent = tpscrolingframe
playertp7.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp7.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp7.BorderSizePixel = 2
playertp7.Position = UDim2.new(0, 0, 0.48, 0)
playertp7.Size = UDim2.new(0, 200, 0, 60)
playertp7.Font = Enum.Font.Highway
playertp7.FontSize = Enum.FontSize.Size28
playertp7.Text = "no player"
playertp7.TextColor3 = Color3.new(1, 1, 1)
playertp7.TextSize = 25
playertp7.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp7.TextStrokeTransparency = 0


playertp8.Parent = tpscrolingframe
playertp8.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp8.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp8.BorderSizePixel = 2
playertp8.Position = UDim2.new(0, 0, 0.56, 0)
playertp8.Size = UDim2.new(0, 200, 0, 60)
playertp8.Font = Enum.Font.Highway
playertp8.FontSize = Enum.FontSize.Size28
playertp8.Text = "no player"
playertp8.TextColor3 = Color3.new(1, 1, 1)
playertp8.TextSize = 25
playertp8.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp8.TextStrokeTransparency = 0


playertp9.Parent = tpscrolingframe
playertp9.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp9.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp9.BorderSizePixel = 2
playertp9.Position = UDim2.new(0, 0, 0.64, 0)
playertp9.Size = UDim2.new(0, 200, 0, 60)
playertp9.Font = Enum.Font.Highway
playertp9.FontSize = Enum.FontSize.Size28
playertp9.Text = "no player"
playertp9.TextColor3 = Color3.new(1, 1, 1)
playertp9.TextSize = 25
playertp9.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp9.TextStrokeTransparency = 0


playertp10.Parent = tpscrolingframe
playertp10.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp10.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp10.BorderSizePixel = 2
playertp10.Position = UDim2.new(0, 0, 0.72, 0)
playertp10.Size = UDim2.new(0, 200, 0, 60)
playertp10.Font = Enum.Font.Highway
playertp10.FontSize = Enum.FontSize.Size28
playertp10.Text = "no player"
playertp10.TextColor3 = Color3.new(1, 1, 1)
playertp10.TextSize = 25
playertp10.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp10.TextStrokeTransparency = 0


playertp11.Parent = tpscrolingframe
playertp11.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
playertp11.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
playertp11.BorderSizePixel = 2
playertp11.Position = UDim2.new(0, 0, 0.80, 0)
playertp11.Size = UDim2.new(0, 200, 0, 60)
playertp11.Font = Enum.Font.Highway
playertp11.FontSize = Enum.FontSize.Size28
playertp11.Text = "no player"
playertp11.TextColor3 = Color3.new(1, 1, 1)
playertp11.TextSize = 25
playertp11.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
playertp11.TextStrokeTransparency = 0








tptoshriff.Parent = teleportFrame
tptoshriff.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
tptoshriff.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
tptoshriff.BorderSizePixel = 2
tptoshriff.Position = UDim2.new(0.52380958, 0, 0.20192119, 0)
tptoshriff.Size = UDim2.new(0, 200, 0, 60)
tptoshriff.Font = Enum.Font.Highway
tptoshriff.FontSize = Enum.FontSize.Size28
tptoshriff.Text = "Sheriff"
tptoshriff.TextColor3 = Color3.new(1, 1, 1)
tptoshriff.TextSize = 25
tptoshriff.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
tptoshriff.TextStrokeTransparency = 0



killAll.Parent = BG
killAll.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
killAll.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
killAll.BorderSizePixel = 2
killAll.Position = UDim2.new(0.022380958, 0, 0.074192119, 0)
killAll.Size = UDim2.new(0, 200, 0, 60)
killAll.Font = Enum.Font.Highway
killAll.FontSize = Enum.FontSize.Size28
killAll.Text = "Killall"
killAll.TextColor3 = Color3.new(1, 1, 1)
killAll.TextSize = 25
killAll.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
killAll.TextStrokeTransparency = 0



StartFarm.Parent = farmScrolingFrame 
StartFarm.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
StartFarm.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
StartFarm.BorderSizePixel = 2
StartFarm.Position = UDim2.new(0.022380958, 0, 0.074192119, 0)
StartFarm.Size = UDim2.new(0, 200, 0, 60)
StartFarm.Font = Enum.Font.Highway
StartFarm.FontSize = Enum.FontSize.Size28
StartFarm.Text = "Start Farm OFF"
StartFarm.TextColor3 = Color3.new(1, 1, 1)
StartFarm.TextSize = 25
StartFarm.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
StartFarm.TextStrokeTransparency = 0

teleportLobby.Parent = teleportFrame
teleportLobby.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
teleportLobby.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
teleportLobby.BorderSizePixel = 2
teleportLobby.Position = UDim2.new(0.022380958, 0, 0.074192119, 0)
teleportLobby.Size = UDim2.new(0, 200, 0, 60)
teleportLobby.Font = Enum.Font.Highway
teleportLobby.FontSize = Enum.FontSize.Size28
teleportLobby.Text = "Lobby"
teleportLobby.TextColor3 = Color3.new(1, 1, 1)
teleportLobby.TextSize = 25
teleportLobby.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
teleportLobby.TextStrokeTransparency = 0


exp.Parent = playerFrame
exp.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
exp.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
exp.BorderSizePixel = 2
exp.Position = UDim2.new(0.022380958, 0, 0.074192119, 0)
exp.Size = UDim2.new(0, 200, 0, 60)
exp.Font = Enum.Font.Highway
exp.FontSize = Enum.FontSize.Size28
exp.Text = "exp"
exp.TextColor3 = Color3.new(1, 1, 1)
exp.TextSize = 25
exp.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
exp.TextStrokeTransparency = 0

noclip.Parent = playerFrame
noclip.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
noclip.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
noclip.BorderSizePixel = 2
noclip.Position = UDim2.new(0.022380958, 0, 0.16192119, 0)
noclip.Size = UDim2.new(0, 200, 0, 60)
noclip.Font = Enum.Font.Highway
noclip.FontSize = Enum.FontSize.Size28
noclip.Text = "noclip OFF"
noclip.TextColor3 = Color3.new(1, 1, 1)
noclip.TextSize = 25
noclip.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
noclip.TextStrokeTransparency = 0

antifling.Parent = playerFrame
antifling.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
antifling.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
antifling.BorderSizePixel = 2
antifling.Position = UDim2.new(0.022380958, 0, 0.24192119, 0)
antifling.Size = UDim2.new(0, 200, 0, 60)
antifling.Font = Enum.Font.Highway
antifling.FontSize = Enum.FontSize.Size28
antifling.Text = "antifling OFF"
antifling.TextColor3 = Color3.new(1, 1, 1)
antifling.TextSize = 25
antifling.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
antifling.TextStrokeTransparency = 0

xray.Parent = playerFrame
xray.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
xray.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
xray.BorderSizePixel = 2
xray.Position = UDim2.new(0.52380958, 0, 0.24192119, 0)
xray.Size = UDim2.new(0, 200, 0, 60)
xray.Font = Enum.Font.Highway
xray.FontSize = Enum.FontSize.Size28
xray.Text = "xray OFF"
xray.TextColor3 = Color3.new(1, 1, 1)
xray.TextSize = 25
xray.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
xray.TextStrokeTransparency = 0



speed.Parent = playerFrame
speed.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
speed.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
speed.BorderSizePixel = 2
speed.Position = UDim2.new(0.64380958, 0, 0.074192119, 0)
speed.Size = UDim2.new(0, 140, 0, 60)
speed.Font = Enum.Font.Highway
speed.FontSize = Enum.FontSize.Size28
speed.Text = "speed OFF"
speed.TextColor3 = Color3.new(1, 1, 1)
speed.TextSize = 20
speed.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
speed.TextStrokeTransparency = 0


jump.Parent = playerFrame
jump.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
jump.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
jump.BorderSizePixel = 2
jump.Position = UDim2.new(0.64380958, 0, 0.16192119, 0)
jump.Size = UDim2.new(0, 140, 0, 60)
jump.Font = Enum.Font.Highway
jump.FontSize = Enum.FontSize.Size28
jump.Text = "jump OFF"
jump.TextColor3 = Color3.new(1, 1, 1)
jump.TextSize = 20
jump.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
jump.TextStrokeTransparency = 0


speedBox.Parent = playerFrame
speedBox.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
speedBox.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
speedBox.BorderSizePixel = 2
speedBox.Position = UDim2.new(0.52380958, 0, 0.074192119, 0)
speedBox.Size = UDim2.new(0, 60, 0, 60)
speedBox.Font = Enum.Font.Highway
speedBox.FontSize = Enum.FontSize.Size28
speedBox.TextColor3 = Color3.new(1, 1, 1)
speedBox.TextSize = 25
speedBox.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
speedBox.TextStrokeTransparency = 0
speedBox.Text = "16"

jumpBox.Parent = playerFrame
jumpBox.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
jumpBox.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
jumpBox.BorderSizePixel = 2
jumpBox.Position = UDim2.new(0.52380958, 0, 0.16192119, 0)
jumpBox.Size = UDim2.new(0, 60, 0, 60)
jumpBox.Font = Enum.Font.Highway
jumpBox.FontSize = Enum.FontSize.Size28
jumpBox.TextColor3 = Color3.new(1, 1, 1)
jumpBox.TextSize = 25
jumpBox.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
jumpBox.TextStrokeTransparency = 0
jumpBox.Text = "50"



hitbox.Parent = BG
hitbox.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
hitbox.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
hitbox.BorderSizePixel = 2
hitbox.Position = UDim2.new(0.52380958, 0, 0.074192119, 0)
hitbox.Size = UDim2.new(0, 200, 0, 60)
hitbox.Font = Enum.Font.Highway
hitbox.FontSize = Enum.FontSize.Size28
hitbox.Text = "HitboxPlayers-50(OFF)"
hitbox.TextColor3 = Color3.new(1, 1, 1)
hitbox.TextSize = 25
hitbox.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
hitbox.TextStrokeTransparency = 0


MoneyHave.Parent = farmScrolingFrame
MoneyHave.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
MoneyHave.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
MoneyHave.BorderSizePixel = 2
MoneyHave.Position = UDim2.new(0.52380958, 0, 0.074192119, 0)
MoneyHave.Size = UDim2.new(0, 200, 0, 60)
MoneyHave.Font = Enum.Font.Highway
MoneyHave.FontSize = Enum.FontSize.Size28
MoneyHave.Text = "Money You Have : "
MoneyHave.TextColor3 = Color3.new(1, 1, 1)
MoneyHave.TextSize = 25
MoneyHave.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
MoneyHave.TextStrokeTransparency = 0




teleportMap.Parent = teleportFrame
teleportMap.BackgroundColor3 = Color3.new(0.486275, 0.611765, 0.419608)
teleportMap.BorderColor3 = Color3.new(0.0392157, 0.352941, 0.0235294)
teleportMap.BorderSizePixel = 2
teleportMap.Position = UDim2.new(0.52380958, 0, 0.074192119, 0)
teleportMap.Size = UDim2.new(0, 200, 0, 60)
teleportMap.Font = Enum.Font.Highway
teleportMap.FontSize = Enum.FontSize.Size28
teleportMap.Text = "map"
teleportMap.TextColor3 = Color3.new(1, 1, 1)
teleportMap.TextSize = 25
teleportMap.TextStrokeColor3 = Color3.new(0.180392, 0, 0.431373)
teleportMap.TextStrokeTransparency = 0



gundropclaim.MouseButton1Click:Connect(function ()

if gundropwork == false then
gundropclaim.Text = "GunAutoClaim ON"
	gundropwork = true 
	while gundropwork == true  do
	local success,error = pcall(function()
		gundropclaim.Text = "GunAutoClaim ON"
	 local roles = game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
	local playerpos = game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame  
	print (playerpos)
	for _, map in pairs(game.workspace:GetChildren()) do 
	if map.Name == "GunDrop" then
	     if roles[game.Players.LocalPlayer.Name] then 
        if roles[game.Players.LocalPlayer.Name].Role == "Murderer" then 
        gundropclaim.Text = "You Are Murderer "
		else
		 gundropclaim.Text = "ClaimGunInProcessed"
		 for _, players in pairs (game.Players:GetChildren()) do 
		 local roles = game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
          if roles[players.Name].Role == "Murderer" then
           local hum1 = players.Character.HumanoidRootPart
		   local hum2 = map
		   local number = (hum1.CFrame - hum2.CFrame).Magnitude
		   print(number)
		   if number > 20  then 
           game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = map.CFrame
		    wait(0.2) 
		    game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = playerpos

		   end 
		   
		   		  end 

		 end 
			
		end 
		 end 
		  

	  end
     for _, gun in pairs(map:GetChildren()) do 
      if gun.Name == "GunDrop" then
		  if roles[game.Players.LocalPlayer.Name] then 
        if roles[game.Players.LocalPlayer.Name].Role == "Murderer" then 
        gundropclaim.Text = "You Are Murderer "
		else
		 gundropclaim.Text = "ClaimGunInProcessed"
		for _, players in pairs (game.Players:GetChildren()) do 
		local roles = game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
          if roles[players.Name].Role == "Murderer" then
           local hum1 = players.Character.HumanoidRootPart
		   local hum2 = gun
		   local number = (hum1.Position - hum2.Position).Magnitude
		   print(number)
		   if number > 20  then 
           game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = gun.CFrame
		    wait(0.2) 
		    game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = playerpos

		   end 
		   
		   		  end 

		 end 
		end 
		 end 
		  
	  end
	end 
	end 
	end)
	
	wait(3)
		
	
	
	
	end
end
if gundropwork == true then
  gundropclaim.Text = "GunAutoClaim OFF"
	gundropwork = false

end
	
end)
killAll.MouseButton1Click:Connect(function()
    if canKillAll == true then 
        canKillAll = false 
        for _, player in pairs(game.Players:GetChildren()) do 
            if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                player.Character:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame 
				player.Character:FindFirstChild("HumanoidRootPart").Anchored = true 
				clickMouse()
				if player.Name == game.Players.LocalPlayer.Name then 
              player.Character:FindFirstChild("HumanoidRootPart").Anchored = false

				end 
				
				
            end
        end 



        killAll.Text = "Wait."
        wait(0.3)
        killAll.Text = "Wait.."
        wait(0.3)
        killAll.Text = "Wait..."
        wait(0.3)
        killAll.Text = "Killall"
		 for _, player in pairs(game.Players:GetChildren()) do 
            if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                
				player.Character:FindFirstChild("HumanoidRootPart").Anchored = false
				
				
            end
        end
        canKillAll = true 
    end 
end)
exp.MouseButton1Click:Connect(function()
    if expwork == false then
        expwork = true 
        while expwork == true do
            wait(0.1)
            
            roles = game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
            
            for _, player in pairs(game.Players:GetPlayers()) do 
                if player.Character then 
                    local highlight = player.Character:FindFirstChild("Highlight")
                    
                    -- Если обводки нет - создаем
                    if not highlight then
                        highlight = Instance.new("Highlight")
                        highlight.Parent = player.Character
                    end
                    
                    
                    if roles[player.Name] then 
                        if roles[player.Name].Role == "Innocent" then 
                            highlight.FillColor = Color3.new(0, 1, 0)
                        elseif roles[player.Name].Role == "Murderer" then 
                            highlight.FillColor = Color3.new(1, 0, 0)
                        elseif roles[player.Name].Role == "Sheriff" then 
                            highlight.FillColor = Color3.new(0, 0, 1)
                        elseif roles[player.Name].Role == "Hero" then 
                            highlight.FillColor = Color3.new(1, 1, 0)
                        else
                            highlight.FillColor = Color3.new(0, 1, 0)
                        end
                    else
                        highlight.FillColor = Color3.new(0.5, 0.5, 0.5)
                    end
                    
                    highlight.OutlineColor = highlight.FillColor
                    highlight.Adornee = player.Character
                end 
            end 
        end
    else 
        expwork = false
        while expwork == false do
            wait(0.1)
            for _, player in pairs(game.Players:GetPlayers()) do 
                if player.Character and player.Character:FindFirstChild("Highlight") then 
                    player.Character:FindFirstChild("Highlight"):Destroy()
                end 
            end
        end
    end
end)

murkill.MouseButton1Click:Connect(function()
if murkillwork == false then
playerpos = game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame  
					murkillwork = true
					murkill.Text = "Killmurder ON"
					
    if mirkillcan == true then 
        mirkillcan = false
       
        
        -- Безопасно получаем данные ролей
        local success, roles = pcall(function()
            return game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
        end)
        
        
        
        -- Проверяем наличие нашего персонажа
        local ourCharacterSuccess, ourCharacter = pcall(function()
            return game.Players.LocalPlayer.Character
        end)
        
       
        
        local foundMurderer = false
        
        for _, player in pairs(game.Players:GetPlayers()) do 
            -- Безопасно проверяем наличие персонажа игрока
            local playerCharSuccess, playerCharacter = pcall(function()
                return player.Character
            end)
            
            if playerCharSuccess and playerCharacter and roles[player.Name] then
			
                if roles[player.Name].Role == "Murderer"  and player.Name ~= game.Players.LocalPlayer.Name then 
                    foundMurderer = true
					
                    while murkillwork == true  do
						  -- Безопасно работаем с HumanoidRootPart
                        local hrpSuccess1, ourHRP = pcall(function()
                            return game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
                        end)
                        
                        local hrpSuccess2, targetHRP = pcall(function()
                            return player.Character:FindFirstChild("Head")
                        end)
                        
                        if hrpSuccess1 and ourHRP and hrpSuccess2 and targetHRP then
                            pcall(function()
							
                                
                                local gg = 0 
								while gg < 15 do 
								gg = gg +1 
								wait(0.01)
								ourHRP.Anchored = false
                              
                                ourHRP.CFrame = targetHRP.CFrame + Vector3.new(10, 0, 0)
                                local camera = game.Workspace.CurrentCamera
                                camera.CFrame = CFrame.new(camera.CFrame.Position, targetHRP.Position)
								end 
								
                                
                                
								
                            end)
                            wait(0.01)
                        else
                            -- Если что-то пошло не так, выходим из цикла
                            break
                        end
					end
                    
                    pcall(function()
                        if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                            player.Character.HumanoidRootPart.Anchored = false
                        end
                    end)
                    
                    
                end
            end 
        end
        
        if not foundMurderer then
            print("Убийца не найден")
        end
        
        -- Анимация завершения
       
        
        mirkillcan = true 
    end
	end 
	if murkillwork == true  then
					murkillwork = false
					wait(0.1)
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = playerpos 
         murkill.Text = "Killmurder OFF"
					end  
end)

speed.MouseButton1Click:Connect(function()
    if speedBox.Text:match("%a") and speedwork == false then
        speed.Text = "pls number"
        wait(0.5)
        speed.Text = "speed OFF"
    else 
        if speedwork == false then 
            speedwork = true 
            speed.Text = "speed ON"
			local cantext = 0 
            while speedwork == true do 
			local speedPl = tonumber(speedBox.Text)
                wait(0.0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001)
                local success, message = pcall(function()
                    if speedBox.Text:match("%a") then
                        speed.Text = "pls number"
                        game.Players.LocalPlayer.Character:FindFirstChild("Humanoid").WalkSpeed = 16 
						if cantext == 1 then 
						cantext = cantext - 1 
						end 
                    else 
					if cantext == 0 then 
                     speed.Text = "speed ON"
					 cantext = cantext + 1 
					end 
					if speedPl >= 0 and speedPl < 101 then 
                        game.Players.LocalPlayer.Character:FindFirstChild("Humanoid").WalkSpeed = speedPl
						else 
						if speedPl <= 0 then
							speedBox.Text = 1

						end
						 if speedPl > 100 then 
                         speedBox.Text = 100
						 
						 end 

						end 
                    end 
                end)
            end 
        else
            if speedBox.Text:match("%a") and speedwork == true then
                -- ничего не делаем если есть буквы
            else 
                speedwork = false
                speed.Text = "speed OFF"
                while speedwork == false do 
                    local success, message = pcall(function()
                        wait(0.000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001)
                        game.Players.LocalPlayer.Character:FindFirstChild("Humanoid").WalkSpeed = 16 
                    end)
                end	
            end
        end 
    end
end)
rolesbutton.MouseButton1Click:Connect(function ()
	playerFrame.Visible = false 
	BG.Visible = true
	teleportFrame.Visible = false
    farmScrolingFrame.Visible = false
end)
buttonFarm.MouseButton1Click:Connect(function ()
	playerFrame.Visible = false 
	farmScrolingFrame.Visible = true
	teleportFrame.Visible = false
    BG.Visible = false 
end)
teleportbutton.MouseButton1Click:Connect(function ()
	playerFrame.Visible = false 
	BG.Visible = false 
	teleportFrame.Visible = true 
    farmScrolingFrame.Visible = false
end)
playerbutton.MouseButton1Click:Connect(function ()
	playerFrame.Visible = true 
	BG.Visible = false 
	teleportFrame.Visible = false
    farmScrolingFrame.Visible = false
end)
hitbox.MouseButton1Click:Connect(function()
    if hitbox100 == false then
        hitbox100 = true
        hitbox.Text = "HitboxPlayers-50(ON)"
        
        while hitbox100 == true do
            for _, player in pairs(game.Players:GetPlayers()) do
                if player ~= game.Players.LocalPlayer then
                    if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                        -- Меняем размер хитбокса
                        player.Character.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
                        player.Character.HumanoidRootPart.Transparency = 0.9
                        -- Создаем обводку в персонаже, а не в HRP
                        if not player.Character:FindFirstChild("HitboxHighlight") then
                            local ss = Instance.new("Highlight")
                            ss.Name = "HitboxHighlight"
                            ss.Adornee = player.Character.HumanoidRootPart
                            ss.FillColor = Color3.new(1, 0, 0)
                            ss.OutlineColor = Color3.new(1, 1, 1)
                            ss.Parent = player.Character
                        end
                    end
                end 
            end
            wait(0.1)
        end
    else 
        hitbox100 = false 
        hitbox.Text = "HitboxPlayers-50(OFF)"
        
        -- Восстанавливаем нормальные размеры
        for _, player in pairs(game.Players:GetPlayers()) do
            if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                player.Character.HumanoidRootPart.Size = Vector3.new(2, 2, 1)
                local highlight = player.Character:FindFirstChild("HitboxHighlight")
                if highlight then
				player.Character.HumanoidRootPart.Transparency = 1
                    highlight:Destroy()
                end
            end
        end
    end
end)
teleportLobby.MouseButton1Click:Connect(function ()
local success,error = pcall(function ()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5008.63721, 305.875, -3.51864505, 1, 0, 0, 0, 1, 0, 0, 0, 1) 
 
end)
	
end)

teleportMap.MouseButton1Click:Connect(function()
    local success, message = pcall(function()
        for _, map in pairs(game.Workspace:GetChildren()) do
		if map.Name ~= "Lobby" then 
            for _, spwn in pairs(map:GetChildren()) do
                if spwn.Name == "Spawns" then
                    local targetpos = spwn.Spawn.CFrame
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetpos
                end
            end
			end
        end
    end)
end)


tptomardered.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
for _, player in pairs (game.Players:GetChildren()) do 
local roles = game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
if roles[player.Name].Role == "Murderer" then 
local targetpos = player.Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetpos

end 

end  
end)
	
end)



tptoshriff.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
for _, player in pairs (game.Players:GetChildren()) do 
local roles = game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
if roles[player.Name].Role == "Sheriff" or roles[player.Name].Role == "Hero" then 
local targetpos = player.Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetpos

end 

end  
end)
	
end)


local UserInputService = game:GetService("UserInputService")
local canE = false
local canEE = true 

UserInputService.InputBegan:Connect(function(input, gameProcessed)
    if gameProcessed then return end -- Игнорируем, если обработано игрой
    
    if input.KeyCode == Enum.KeyCode.E then
	if canEE == true then
	canEE = false  
        print("Клавиша E нажата!")
		if canE ==true  then
         canE = false 
			BG2.Visible =true
			wait(0.5)
			canEE = true
			else
				BG2.Visible = false
			wait(0.5)
			canE = true
			canEE = true
		end
		
        end 
    end
end)


function tpupdate()
task.spawn(function()
while true  do
wait(4)
print("начал")
	local success, message = pcall(function()
     
         local gg = 0
	  for _, players in pairs(game.Players:GetChildren()) do
	  
      if players.Name ~= game.Players.LocalPlayer.Name then 
	  
      if gg == 0 then 
         playertp1.Text = players.Name 
         

	  end 
	  if gg == 1 then 
         playertp2.Text = players.Name 
        

	  end 
	  if gg == 2 then 
         playertp3.Text = players.Name 
         
		  print("уже тут")

	  end 
	  if gg == 3 then 
         playertp4.Text = players.Name 
         

	  end 
	  if gg == 4 then 
         playertp5.Text = players.Name 
       
      
	  end 
	  if gg == 5 then 
         playertp6.Text = players.Name 
      

	  end 
	  if gg == 6 then 
         playertp7.Text = players.Name 
         

	  end 
	  if gg == 7 then 
         playertp8.Text = players.Name 
       

	  end 
	  if gg == 8 then 
         playertp9.Text = players.Name 
         

	  end 
	  if gg == 9 then 
         playertp10.Text = players.Name 
          
	  end 
	  if gg == 10 then 
         playertp11.Text = players.Name 
        

	  end 
      gg = gg+1

	  end 
      end
	end ) 
end
end)
end

playertp1.MouseButton1Click:Connect(function ()
local success, message = pcall(function()

local targetCFrame = game.Players:FindFirstChild(playertp1.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)

playertp2.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp2.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp3.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp3.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp4.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp4.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp5.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp5.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp6.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp6.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp7.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp7.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp8.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp8.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp9.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp9.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp10.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp10.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)



playertp11.MouseButton1Click:Connect(function ()
local success, message = pcall(function()
local targetCFrame = game.Players:FindFirstChild(playertp11.Text).Character.HumanoidRootPart.CFrame
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
end)

end)

jump.MouseButton1Click:Connect(function()
    if jumpBox.Text:match("%a") and jumpwork == false then
        jump.Text = "pls number"
        wait(0.5)
       jump.Text = "jump OFF"
    else 
        if jumpwork == false then 
            jumpwork = true 
            jump.Text = "jump ON"
			local cantext = 0 
            while jumpwork == true do 
			local jumpPl = tonumber(jumpBox.Text)
                wait(0.0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001)
                local success, message = pcall(function()
                    if jumpBox.Text:match("%a") then
                        jump.Text = "pls number"
                        game.Players.LocalPlayer.Character:FindFirstChild("Humanoid").JumpPower = 50
						if cantext == 1 then 
						cantext = cantext - 1 
						end 
                    else 
					if cantext == 0 then 
                     jump.Text = "jump ON"
					 cantext = cantext + 1 
					end 
					if jumpPl >= 0 and jumpPl < 301 then 
                        game.Players.LocalPlayer.Character:FindFirstChild("Humanoid").JumpPower = jumpPl
						else 
						if jumpPl <= 0 then
							jumpBox.Text = 1

						end
						 if jumpPl > 301 then 
                         jumpBox.Text = 300
						 
						 end 

						end 
                    end 
                end)
            end 
        else
            if jumpBox.Text:match("%a") and jumpwork == true then
                -- ничего не делаем если есть буквы
            else 
                jumpwork = false
                jump.Text = "jump OFF"
                while jumpwork == false do 
                    local success, message = pcall(function()
                        wait(0.000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001)
                        game.Players.LocalPlayer.Character:FindFirstChild("Humanoid").JumpPower = 50 
                    end)
                end	
            end
        end 
    end
end)

noclip.MouseButton1Click:Connect(function ()
if noclipwork == false then 
noclipwork = true 
noclip.Text = "noclip ON"
while noclipwork == true do
wait(0.1)
	local success, message = pcall(function()
	
	for _, part in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
    if part:IsA("BasePart") then 
    part.CanCollide = false 
	end 
	end 
	
	end)
end
else
noclipwork = false 
noclip.Text = "noclip OFF"
	for _, part in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
    if part:IsA("BasePart") then 
    part.CanCollide = true 


	end 
	
	end 



end 


	
end)
local antiflingwork = false 

antifling.MouseButton1Click:Connect(function ()
	if antiflingwork == false then 
	antifling.Text = "antifling ON"
    antiflingwork = true 
	while antiflingwork == true do 
	wait(0.0000001)
	local success, message = pcall( function()
    for _, player in pairs(game.Players:GetChildren()) do 
   if player.Name ~= game.Players.LocalPlayer.Name then 
   for _, part in pairs(player.Character:GetChildren()) do 
     if part:IsA("BasePart") then 
    part.CanCollide = false 

	 end 

   end 

   end 
	end 

    end)
	end 

	
 else 
antifling.Text = "antifling OFF"
    antiflingwork = false 
	for _, player in pairs(game.Players:GetChildren()) do 
   if player.Name ~= game.Players.LocalPlayer.Name then 
   for _, part in pairs(player.Character:GetChildren()) do 
     if part:IsA("BasePart") then 
    part.CanCollide = true  

	 end 

   end 

   end 
	end 
end 
end)


xray.MouseButton1Click:Connect(function ()


	if xraywork == false then
		xraywork = true 
         xray.Text = "xray ON"
		while xraywork == true do
		
		     

			local success, message = pcall( function()
			  function makeXRayPart(part)
	
	part.Transparency = 0.8
end

 function recurseForParts(object)
	-- Мы нашли часть, которая не является 
	if object:IsA("BasePart") then
	if object.Transparency ~= 1 then 
		makeXRayPart(object)
		end 
	end

	-- Остановимся, если у этого объекта есть Humanoid - мы не хотим видеть игроков! 
	if object:FindFirstChild("Humanoid") then return end

	-- Проверяем детей объекта на наличие других частей
	for _, child in pairs(object:GetChildren()) do
		recurseForParts(child)
	end
end

recurseForParts(game.workspace)
			end )
			wait(20)
		end
       

		else 
		 function makeXRayPart(part)
	
	part.Transparency = 0
end

 function recurseForParts(object)
	-- Мы нашли часть, которая не является 
	if object:IsA("BasePart") then
	if object.Transparency ~= 1 then 
		makeXRayPart(object)
		end 
	end

	-- Остановимся, если у этого объекта есть Humanoid - мы не хотим видеть игроков! 
	if object:FindFirstChild("Humanoid") then return end

	-- Проверяем детей объекта на наличие других частей
	for _, child in pairs(object:GetChildren()) do
		recurseForParts(child)
	end
end

recurseForParts(game.workspace)
         xraywork = false
		 xray.Text = "xray OFF"
		
		
	end


end)


local canclickstartfarm = 0

StartFarm.MouseButton1Click:Connect(function()
  if canclickstartfarm == 1 then
   
     
       StartFarm.Text = "Start Farm OFF"
       farmEnable = false

       canclickstartfarm = 0
       else
        farmEnable = true
        StartFarm.Text = "Start Farm ON"
        canclickstartfarm = 1
        

end
end)





game.Players.LocalPlayer.Idled:Connect(function()
    VirtualUser:CaptureController()
    VirtualUser:ClickButton2(Vector2.new())
end)

function number(coin)
if farmEnable == true then 
local success, message = pcall( function()
    local num = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - coin.Position).Magnitude
	
    if num < posmin and coin.CoinVisual.Transparency == 0  then 
        posmin = num 
        targetcoin = {CFrame = coin.CFrame}
        coin2 = coin 
    end
	end)

    end
end 

function coininfolder()

local success, message = pcall( function()
    posmin = 999999999
    targetcoin = nil
    coin2 = nil
    for _, coin in pairs(folder:GetChildren()) do 
        number(coin)
    end 
	end)
end
 
function farm ()
task.spawn(function()
while true do

wait() 
if farmEnable == true then

local success, message = pcall( function()

    if farmwork == true then
        coininfolder()
      
        if   game.Players.LocalPlayer.PlayerGui.MainGUI.Game.CoinBags.Container.SnowToken.CurrencyFrame.Icon.Coins.Text ~= "50" and game.Players.LocalPlayer.PlayerGui.MainGUI.Game.CoinBags.Container.SnowToken.Visible == true  then
            
            -- ПРОВЕРКА ПЕРЕД ПОЛЕТОМ: МОНЕТКА СУЩЕСТВУЕТ И ВАЛИДНА
            if not coin2 or not coin2.Parent or not coin2:FindFirstChild("CoinVisual") or coin2.CoinVisual.Transparency > 0 then
                -- НЕ ВКЛЮЧАЕМ mes, ПРОСТО ИЩЕМ ДРУГУЮ МОНЕТКУ
                wait(0.1)
                return
            end
            
            local realDistance = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - coin2.Position).Magnitude
            
            -- ЗАЩИТА: НЕ ЛЕТАТЬ К МОНЕТКАМ КОТОРЫЕ СЛИШКОМ ДАЛЕКО
            if realDistance > 1000 then
                wait(0.1)
                return
            end
            
            local flyTime = realDistance / 25
            
            -- ОГРАНИЧЕНИЕ МАКСИМАЛЬНОГО ВРЕМЕНИ ПОЛЕТА
            if flyTime > 5 then
                flyTime = 5
            end
            
            animationSettings = TweenInfo.new(flyTime, Enum.EasingStyle.Linear)
            
            -- СОХРАНЯЕМ КОПИЮ CFrame ПЕРЕД ПОЛЕТОМ
             local targetCFrameCopy = coin2.CFrame * CFrame.new(0, -1.5, 0)
            
            -- ПРОВЕРКА НА НЕВАЛИДНЫЙ CFrame (NaN)
            if targetCFrameCopy.X ~= targetCFrameCopy.X or targetCFrameCopy.Y ~= targetCFrameCopy.Y or targetCFrameCopy.Z ~= targetCFrameCopy.Z then
                wait(0.1)
                return
            end
            
            local movement = twins:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, animationSettings, {CFrame = targetCFrameCopy})
			
            movement:Play()
            
            -- Проверяем прозрачность во время полета
            local startTime = tick() 
            while tick() - startTime < flyTime do
                if not coin2 or not coin2.Parent or not coin2:FindFirstChild("CoinVisual") or coin2.CoinVisual.Transparency > 0 then
                    movement:Cancel()
                    break
                end
                wait(flyTime/11)
            end
        else
            -- ВОТ ТУТ РАУНД ЗАКОНЧИЛСЯ ИЛИ 50 МОНЕТ
            MurFling()
            coin2 = nil
            farmwork = false
            mes = true  -- ТОЛЬКО ЗДЕСЬ ВКЛЮЧАЕМ СООБЩЕНИЯ
        end
    else
    
        -- Проверяем, можно ли снова фармить
        if mes == true then
            mes = false -- СРАЗУ СБРАСЫВАЕМ ФЛАГ ЧТОБЫ НЕ СПАМИТЬ
            if mescan == true then 
                -- ОДНО СЛУЧАЙНОЕ СООБЩЕНИЕ
                local num = math.random(1,20)
                if num == 1 then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("farm") 
                elseif num == 2  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("f")
                elseif num == 3  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("gg")
                elseif num == 4  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("ss")
                elseif num == 5  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("what")
                elseif num == 6  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("kill")
                elseif num == 7  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("remove")
                elseif num == 8  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("dd")
                elseif num == 9  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("aa")
                elseif num == 10  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("qq")
                elseif num == 11  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("oo")
                elseif num == 12  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("pp")
                elseif num == 13  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("kl")
                elseif num == 14  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("function")
                elseif num == 15  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("hello")
                elseif num == 16  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("qw")
                elseif num == 17  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("sad")
                elseif num == 18  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("funny")
                elseif num == 19  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("noo")
                elseif num == 20  then 
                    game:GetService("TextChatService").TextChannels.RBXGeneral:SendAsync("pls")
                end 
            end 
        end
        
        if game.Players.LocalPlayer.PlayerGui.MainGUI.Game.CoinBags.Container.SnowToken.Visible == true 
           and game.Players.LocalPlayer.PlayerGui.MainGUI.Game.CoinBags.Container.SnowToken.CurrencyFrame.Icon.Coins.Text ~= "50" 
           and game.Players.LocalPlayer.PlayerGui.MainGUI.Game.CoinBags.Container.SnowToken.Full.Visible ~= true then
            
            -- ПЕРЕД ВКЛЮЧЕНИЕМ ФАРМА ИЩЕМ FOLDER ЗАНОВО
            for _, part in pairs(game.workspace:GetChildren()) do 
                for _, gamefolder in pairs(part:GetChildren()) do 
                    if gamefolder.Name == "CoinContainer" then 
                        folder = gamefolder
                    end 
                end 
            end 
            
            farmwork = true
        end
    end
end)

end
end 
end)
end

-- Запуск фарма
farm()

local canclickprint = 0
printifautofarmstopped.MouseButton1Click:Connect(function()
if canclickprint == 0 then 
canclickprint = 1
mescan = true
printifautofarmstopped.Text = "Print ON"
else
mescan = false
canclickprint = 0
printifautofarmstopped.Text = "Print OFF"
end
end)


local canx2 = 0 
resetifmes.MouseButton1Click:Connect(function()
if canx2 == 0 then 
killifmesenge = true
resetifmes.Text = "kill if print ON"
canx2 = 1 
else
killifmesenge = false
resetifmes.Text = "kill if print OFF"
canx2 = 0

end 


end)

local player = game.Players.LocalPlayer
local commands = {"farm","f","gg","ss","what","kill","remove","dd","aa","qq","oo","pp","kl","function","hello","qw","sad","funny","noo","pls"}

game:GetService("TextChatService").MessageReceived:Connect(function(msg)
if killifmesenge == true then 
    for _,cmd in pairs(commands) do
        if msg.Text:lower() == cmd and player.Character then
            local h = player.Character:FindFirstChild("Humanoid")
            if h then h.Health = 0 end
            break
        end
    end
    end 
end)

local function SkidFlingToDeath(TargetPlayer)
    local Character = game.Players.LocalPlayer.Character
    local Humanoid = Character and Character:FindFirstChildOfClass("Humanoid")
    local RootPart = Humanoid and Humanoid.RootPart
    local TCharacter = TargetPlayer.Character
    
    if not TCharacter then return false end
    
    local THumanoid = TCharacter:FindFirstChildOfClass("Humanoid")
    if not THumanoid or THumanoid.Health <= 0 then
        return false  -- Мардер уже мертв
    end
    
    -- Сохраняем старую позицию
    if RootPart and RootPart.Velocity.Magnitude < 50 then
        getgenv().OldPos = RootPart.CFrame
    end
    
    local TRootPart = THumanoid and THumanoid.RootPart
    local THead = TCharacter:FindFirstChild("Head")
    
    if not Character or not Humanoid or not RootPart then
        return false
    end
    
    -- Сохраняем высоту уничтожения
    getgenv().FPDH = workspace.FallenPartsDestroyHeight
    workspace.FallenPartsDestroyHeight = 0/0
    
    local BV = Instance.new("BodyVelocity")
    BV.Parent = RootPart
    BV.Velocity = Vector3.new(0, 0, 0)
    BV.MaxForce = Vector3.new(9e9, 9e9, 9e9)
    
    Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
    
    local function FPos(BasePart, Pos, Ang)
        if not BasePart or not BasePart.Parent then return end
        RootPart.CFrame = CFrame.new(BasePart.Position) * Pos * Ang
        Character:SetPrimaryPartCFrame(CFrame.new(BasePart.Position) * Pos * Ang)
        RootPart.Velocity = Vector3.new(9e7, 9e7 * 10, 9e7)
        RootPart.RotVelocity = Vector3.new(9e8, 9e8, 9e8)
    end
    
    local BasePart = TRootPart or THead
    if not BasePart then
        BV:Destroy()
        workspace.FallenPartsDestroyHeight = getgenv().FPDH
        return false
    end
    
    -- Флингаем пока мардер жив
    while THumanoid and THumanoid.Health > 0 and BasePart and BasePart.Parent do
        local TimeToWait = 1  -- Укороченное время для более частых циклов
        local Time = tick()
        local Angle = 0
        
        repeat
            if not THumanoid or THumanoid.Health <= 0 then break end
            if not RootPart or not THumanoid then break end
            
            if BasePart.Velocity.Magnitude < 50 then
                Angle = Angle + 100
                FPos(BasePart, CFrame.new(0, 1.5, 0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25, CFrame.Angles(math.rad(Angle), 0, 0))
                task.wait()
                FPos(BasePart, CFrame.new(0, -1.5, 0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25, CFrame.Angles(math.rad(Angle), 0, 0))
                task.wait()
            else
                FPos(BasePart, CFrame.new(0, 1.5, THumanoid.WalkSpeed), CFrame.Angles(math.rad(90), 0, 0))
                task.wait()
                FPos(BasePart, CFrame.new(0, -1.5, -THumanoid.WalkSpeed), CFrame.Angles(0, 0, 0))
                task.wait()
            end
        until Time + TimeToWait < tick() or (THumanoid and THumanoid.Health <= 0)
    end
    
    -- Восстановление
    BV:Destroy()
    Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
    
    -- Возвращаем на старую позицию если мардер умер
    if getgenv().OldPos and (not THumanoid or THumanoid.Health <= 0) then
        repeat
            RootPart.CFrame = getgenv().OldPos * CFrame.new(0, .5, 0)
            Character:SetPrimaryPartCFrame(getgenv().OldPos * CFrame.new(0, .5, 0))
            Humanoid:ChangeState("GettingUp")
            for _, part in pairs(Character:GetChildren()) do
                if part:IsA("BasePart") then
                    part.Velocity, part.RotVelocity = Vector3.new(), Vector3.new()
                end
            end
            task.wait()
        until (RootPart.Position - getgenv().OldPos.p).Magnitude < 25
    end
    
    workspace.FallenPartsDestroyHeight = getgenv().FPDH
    
    return (not THumanoid or THumanoid.Health <= 0)  -- Возвращает true если мардер умер
end

-- 2. Функция поиска мардера
local function FindMurderer()
    local success, roles = pcall(function()
        return game.ReplicatedStorage:FindFirstChild("GetPlayerData", true):InvokeServer()
    end)
    
    if success and roles then
        for playerName, data in pairs(roles) do
            if data.Role == "Murderer" then
                local player = game.Players:FindFirstChild(playerName)
                if player and player.Character then
                if playerName ~= game.Players.LocalPlayer.Name then 
                    return player
                    else
                    game.Players.LocalPlayer.Character.Humanoid.Health = 0 
                    end
                end
            end
        end
    end
    return nil
end

-- 3. ОСНОВНАЯ ФУНКЦИЯ - флингает мардера до смерти
function MurFling()
    local murderer = FindMurderer()
    
    if not murderer then
        print("[MurFling] Мардер не найден")
        return
    end
    
    print("[MurFling] Найден мардер: " .. murderer.Name)
    
    -- Получаем Humanoid мардера
    local murdererHumanoid = murderer.Character and murderer.Character:FindFirstChildOfClass("Humanoid")
    if not murdererHumanoid then
        print("[MurFling] У мардера нет Humanoid")
        return
    end
    
    -- Флингаем пока мардер жив
    while murdererHumanoid and murdererHumanoid.Health > 0 do
        -- Обновляем ссылки (на случай респавна)
        if not murderer.Character or not murderer.Character.Parent then
            murderer = FindMurderer()
            if not murderer then break end
            murdererHumanoid = murderer.Character and murderer.Character:FindFirstChildOfClass("Humanoid")
            if not murdererHumanoid then break end
        end
        
        -- Выполняем флинг в стиле KILASIK
        local killed = SkidFlingToDeath(murderer)
        
        -- Если флинг завершился и мардер еще жив, продолжаем
        if not killed and murdererHumanoid and murdererHumanoid.Health > 0 then
            wait(0.5)  -- Краткая пауза перед следующим циклом флинга
        else
            break  -- Мардер умер или произошла ошибка
        end
    end
    
    print("[MurFling] Мардер убит!")
end

print("lol")
farm ()
tpupdate() 

wait(3)
