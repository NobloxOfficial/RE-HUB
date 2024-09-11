-- Function to create the notifier GUI
local function createNotifier()
    -- Create ScreenGui
    local screenGui = Instance.new("ScreenGui")
    screenGui.Name = "Notifier"
    screenGui.Parent = game.CoreGui
 
    -- Create Frame
    local frame = Instance.new("Frame")
    frame.Size = UDim2.new(0, 320, 0, 120)
    frame.Position = UDim2.new(0.5, -160, 0, 50)
    frame.BackgroundColor3 = Color3.fromRGB(30, 30, 30) -- Dark grey background
    frame.BorderSizePixel = 2
    frame.BorderColor3 = Color3.fromRGB(0, 0, 0) -- Black border
    frame.Parent = screenGui
 
    -- Add UICorner to Frame
    local frameCorner = Instance.new("UICorner")
    frameCorner.CornerRadius = UDim.new(0, 10)
    frameCorner.Parent = frame
 
    -- Add UIGradient to Frame
    local frameGradient = Instance.new("UIGradient")
    frameGradient.Color = ColorSequence.new{
        ColorSequenceKeypoint.new(0, Color3.fromRGB(45, 45, 45)),
        ColorSequenceKeypoint.new(1, Color3.fromRGB(30, 30, 30))
    }
    frameGradient.Parent = frame
 
    -- Create Label
    local label = Instance.new("TextLabel")
    label.Size = UDim2.new(1, -40, 0, 50)
    label.Position = UDim2.new(0, 20, 0, 20)
    label.BackgroundTransparency = 1
    label.Text = "RE Script Hub Loaded Successfully"
    label.TextColor3 = Color3.fromRGB(0, 255, 0) -- Green text
    label.Font = Enum.Font.GothamBold
    label.TextSize = 18
    label.TextWrapped = true
    label.Parent = frame
 
    -- Create Close Button
    local closeButton = Instance.new("TextButton")
    closeButton.Size = UDim2.new(0, 30, 0, 30)
    closeButton.Position = UDim2.new(1, -40, 0, 10)
    closeButton.BackgroundColor3 = Color3.fromRGB(255, 0, 0) -- Red background
    closeButton.BorderSizePixel = 2
    closeButton.BorderColor3 = Color3.fromRGB(0, 0, 0) -- Black border
    closeButton.Text = "X"
    closeButton.TextColor3 = Color3.fromRGB(255, 255, 255) -- White text
    closeButton.Font = Enum.Font.GothamBold
    closeButton.TextSize = 20
    closeButton.Parent = frame
 
    -- Add UICorner to Close Button
    local closeButtonCorner = Instance.new("UICorner")
    closeButtonCorner.CornerRadius = UDim.new(0, 10)
    closeButtonCorner.Parent = closeButton
 
    -- Function to close the notifier
    local function closeNotifier()
        screenGui:Destroy()
    end
 
    -- Connect Close Button
    closeButton.MouseButton1Click:Connect(closeNotifier)
 
    -- Automatically close after 10 seconds
    delay(10, closeNotifier)
end
 
-- Call the function to create the notifier
createNotifier()
 
print("RE Script Hub Loaded Successfully")
 
-- Create ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "REHub"
screenGui.Parent = game.CoreGui
 
-- Create Frame
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 400, 0, 500)
frame.Position = UDim2.new(0.5, -200, 0.5, -250)
frame.BackgroundColor3 = Color3.fromRGB(40, 40, 40) -- Dark grey background
frame.BorderSizePixel = 2
frame.BorderColor3 = Color3.fromRGB(0, 0, 0) -- Black border
frame.Active = true
frame.Draggable = true
frame.Parent = screenGui
 
-- Add UICorner to Frame
local frameCorner = Instance.new("UICorner")
frameCorner.CornerRadius = UDim.new(0, 15)
frameCorner.Parent = frame
 
-- Add UIGradient to Frame
local frameGradient = Instance.new("UIGradient")
frameGradient.Color = ColorSequence.new{
    ColorSequenceKeypoint.new(0, Color3.fromRGB(50, 50, 50)),
    ColorSequenceKeypoint.new(1, Color3.fromRGB(30, 30, 30))
}
frameGradient.Parent = frame
 
-- Create Scrolling Frame
local scrollingFrame = Instance.new("ScrollingFrame")
scrollingFrame.Size = UDim2.new(1, 0, 1, -60)
scrollingFrame.Position = UDim2.new(0, 0, 0, 60)
scrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 600) -- Adjust this value based on the number of buttons
scrollingFrame.ScrollBarThickness = 10
scrollingFrame.BackgroundColor3 = Color3.fromRGB(45, 45, 45) -- Dark grey background
scrollingFrame.BorderSizePixel = 2
scrollingFrame.BorderColor3 = Color3.fromRGB(0, 0, 0) -- Black border
scrollingFrame.Parent = frame
 
-- Add UICorner to Scrolling Frame
local scrollingFrameCorner = Instance.new("UICorner")
scrollingFrameCorner.CornerRadius = UDim.new(0, 10)
scrollingFrameCorner.Parent = scrollingFrame
 
-- Create Label
local label = Instance.new("TextLabel")
label.Size = UDim2.new(1, 0, 0, 60)
label.Position = UDim2.new(0, 0, 0, 0)
label.BackgroundColor3 = Color3.fromRGB(30, 30, 30) -- Darker grey background
label.BorderSizePixel = 2
label.BorderColor3 = Color3.fromRGB(0, 0, 0) -- Black border
label.Text = "RE Hub"
label.TextColor3 = Color3.fromRGB(0, 255, 0) -- Green text
label.Font = Enum.Font.GothamBold
label.TextSize = 28
label.Parent = frame
 
-- Add UICorner to Label
local labelCorner = Instance.new("UICorner")
labelCorner.CornerRadius = UDim.new(0, 10)
labelCorner.Parent = label
 
-- Function to create buttons
local function createButton(name, position, script)
    local button = Instance.new("TextButton")
    button.Size = UDim2.new(1, -20, 0, 50)
    button.Position = UDim2.new(0, 10, 0, position)
    button.BackgroundColor3 = Color3.fromRGB(60, 60, 60) -- Slightly lighter grey background
    button.BorderSizePixel = 2
    button.BorderColor3 = Color3.fromRGB(0, 0, 0) -- Black border
    button.Text = name
    button.TextColor3 = Color3.fromRGB(255, 255, 255) -- White text
    button.Font = Enum.Font.Gotham
    button.TextSize = 22
    button.MouseButton1Click:Connect(function()
        loadstring(game:HttpGet(script))()
    end)
    button.Parent = scrollingFrame
 
    -- Add UICorner to Button
    local buttonCorner = Instance.new("UICorner")
    buttonCorner.CornerRadius = UDim.new(0, 10)
    buttonCorner.Parent = button
end
 
-- Create Buttons
createButton("Arsenal", 10, "https://raw.githubusercontent.com/tbao143/thaibao/main/TbaoHubArsenal")
createButton("Doors Floor 1 and 2 V1", 70, "https://raw.githubusercontent.com/KINGHUB01/BlackKing-obf/main/Doors%20Blackking%20And%20BobHub")
createButton("Doors Floor 1 and 2 V2", 130, "https://raw.githubusercontent.com/FFJ1/Roblox-Exploits/main/scripts/Loader.lua")
createButton("Serenade HUB", 190, "https://raw.githubusercontent.com/4xdhondiscord/SerenadeHub/main/Serenade")
createButton("BladeBall Auto PARRY GUI", 250, "https://raw.githubusercontent.com/FFJ1/Roblox-Exploits/main/scripts/autoparry.lua")
createButton("INF YIELD V6", 310, "https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source")
createButton("DARK DEX V3", 370, "https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/BypassedDarkDexV3.lua")
 
-- Create Minimize Button
local minimizeButton = Instance.new("TextButton")
minimizeButton.Size = UDim2.new(0, 30, 0, 30)
minimizeButton.Position = UDim2.new(1, -70, 0, 10)
minimizeButton.BackgroundColor3 = Color3.fromRGB(255, 255, 0) -- Yellow background
minimizeButton.BorderSizePixel = 2
minimizeButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
