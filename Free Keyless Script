-- =============================================
-- ACHIESON HUB — FULLY WORKING VERSION
-- =============================================

local CoreGui = game:GetService("CoreGui")
local TweenService = game:GetService("TweenService")
local UserInputService = game:GetService("UserInputService")

-- EDIT YOUR LINKS
local DISCORD_LINK = "https://discord.gg/SGtngNuUD"
local SCRIPT_LINK = "loadstring(game:HttpGet('https://raw.githubusercontent.com/Owl-Hub-premium/Scripts/refs/heads/main/Mainloader.lua'))()"

-- Clear old
if CoreGui:FindFirstChild("MirandaHubPopup") then
    CoreGui.MirandaHubPopup:Destroy()
end

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "MirandaHubPopup"
ScreenGui.ResetOnSpawn = false
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.Parent = CoreGui

-- MAIN FRAME
local MainFrame = Instance.new("Frame")
MainFrame.Size = UDim2.new(0, 340, 0, 165)
MainFrame.Position = UDim2.new(0.5, -170, 0.5, -82)
MainFrame.BackgroundColor3 = Color3.fromRGB(15, 15, 18)
MainFrame.BorderSizePixel = 2
MainFrame.BorderColor3 = Color3.fromRGB(220, 40, 40)
MainFrame.ClipsDescendants = true
MainFrame.Parent = ScreenGui

Instance.new("UICorner", MainFrame).CornerRadius = UDim.new(0, 8)

-- Red Divider Line
local TopLine = Instance.new("Frame")
TopLine.Size = UDim2.new(0.9, 0, 0, 2)
TopLine.Position = UDim2.new(0.05, 0, 0, 42)
TopLine.BackgroundColor3 = Color3.fromRGB(220, 40, 40)
TopLine.Parent = MainFrame

-- Title: ACHIESON HUB — LEFT
local TitleLabel = Instance.new("TextLabel")
TitleLabel.Size = UDim2.new(0.65, 0, 0, 35)
TitleLabel.Position = UDim2.new(0.05, 0, 0, 2)
TitleLabel.BackgroundTransparency = 1
TitleLabel.Text = "ACHIESON HUB"
TitleLabel.TextColor3 = Color3.fromRGB(220, 40, 40)
TitleLabel.TextSize = 20
TitleLabel.Font = Enum.Font.GothamBlack
TitleLabel.TextXAlignment = Enum.TextXAlignment.Left
TitleLabel.Parent = MainFrame

-- UPDATED!!! — RIGHT SIDE
local UpdateLabel = Instance.new("TextLabel")
UpdateLabel.Size = UDim2.new(0.28, 0, 0, 35)
UpdateLabel.Position = UDim2.new(0.60, 0, 0, 2)
UpdateLabel.BackgroundTransparency = 1
UpdateLabel.Text = "UPDATED!!!"
UpdateLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
UpdateLabel.TextSize = 15
UpdateLabel.Font = Enum.Font.GothamBold
UpdateLabel.TextXAlignment = Enum.TextXAlignment.Right
UpdateLabel.Parent = MainFrame

-- CLOSE BUTTON — CLEAN X
local CloseBtn = Instance.new("TextButton")
CloseBtn.Size = UDim2.new(0, 26, 0, 26)
CloseBtn.Position = UDim2.new(1, -32, 0, 8)
CloseBtn.BackgroundTransparency = 1
CloseBtn.Text = "X"
CloseBtn.TextColor3 = Color3.fromRGB(180, 180, 180)
CloseBtn.TextSize = 14
CloseBtn.Font = Enum.Font.GothamBold
CloseBtn.AutoLocalize = false
CloseBtn.Parent = MainFrame

-- Message
local MessageLabel = Instance.new("TextLabel")
MessageLabel.Size = UDim2.new(0.9, 0, 0, 28)
MessageLabel.Position = UDim2.new(0.05, 0, 0, 52)
MessageLabel.BackgroundTransparency = 1
MessageLabel.Text = "COPY THE NEW UPDATED SCRIPT AND EXECUTE AGAIN."
MessageLabel.TextColor3 = Color3.fromRGB(160, 160, 160)
MessageLabel.TextSize = 11
MessageLabel.Font = Enum.Font.Gotham
MessageLabel.Parent = MainFrame

-- COPY SCRIPT — LEFT
local CopyScriptBtn = Instance.new("TextButton")
CopyScriptBtn.Size = UDim2.new(0.43, 0, 0, 38)
CopyScriptBtn.Position = UDim2.new(0.05, 0, 0, 105)
CopyScriptBtn.BackgroundColor3 = Color3.fromRGB(50, 100, 255)
CopyScriptBtn.Text = "COPY SCRIPT"
CopyScriptBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
CopyScriptBtn.TextSize = 12
CopyScriptBtn.Font = Enum.Font.GothamBold
CopyScriptBtn.AutoLocalize = false
CopyScriptBtn.Parent = MainFrame

Instance.new("UICorner", CopyScriptBtn).CornerRadius = UDim.new(0, 6)

-- COPY DISCORD — RIGHT
local CopyDiscordBtn = Instance.new("TextButton")
CopyDiscordBtn.Size = UDim2.new(0.43, 0, 0, 38)
CopyDiscordBtn.Position = UDim2.new(0.52, 0, 0, 105)
CopyDiscordBtn.BackgroundColor3 = Color3.fromRGB(50, 100, 255)
CopyDiscordBtn.Text = "COPY DISCORD"
CopyDiscordBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
CopyDiscordBtn.TextSize = 12
CopyDiscordBtn.Font = Enum.Font.GothamBold
CopyDiscordBtn.AutoLocalize = false
CopyDiscordBtn.Parent = MainFrame

Instance.new("UICorner", CopyDiscordBtn).CornerRadius = UDim.new(0, 6)

-- Copy Helper
local function copyToClipboard(text)
    if setclipboard then
        setclipboard(text)
        return true
    end
    return pcall(function()
        local t = Instance.new("TextBox")
        t.Text = text
        t.Visible = false
        t.Parent = CoreGui
        t:CaptureFocus()
        t:SelectAll()
        UserInputService:CopyClipboard()
        t:Destroy()
    end)
end

-- Script Button
CopyScriptBtn.MouseButton1Click:Connect(function()
    if copyToClipboard(SCRIPT_LINK) then
        CopyScriptBtn.Text = "✅ COPIED!"
        CopyScriptBtn.BackgroundColor3 = Color3.fromRGB(40, 180, 80)
        task.delay(2.5, function()
            CopyScriptBtn.Text = "COPY SCRIPT"
            CopyScriptBtn.BackgroundColor3 = Color3.fromRGB(50, 100, 255)
        end)
    end
end)

-- Discord Button
CopyDiscordBtn.MouseButton1Click:Connect(function()
    if copyToClipboard(DISCORD_LINK) then
        CopyDiscordBtn.Text = "✅ COPIED!"
        CopyDiscordBtn.BackgroundColor3 = Color3.fromRGB(40, 180, 80)
        task.delay(2.5, function()
            CopyDiscordBtn.Text = "COPY DISCORD"
            CopyDiscordBtn.BackgroundColor3 = Color3.fromRGB(50, 100, 255)
        end)
    end
end)

-- Close with animation
CloseBtn.MouseButton1Click:Connect(function()
    local tween = TweenService:Create(MainFrame, TweenInfo.new(0.25, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {
        Transparency = 1,
        Position = UDim2.new(0.5, -170, 0.5, -200)
    })
    tween:Play()
    tween.Completed:Connect(function()
        ScreenGui:Destroy()
    end)
end)
