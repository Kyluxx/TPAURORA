local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")

local player = Players.LocalPlayer

local locations = {
	{pos = Vector3.new(-1813, -137, -3281), name = "Brine Pool"},
	{pos = Vector3.new(-1836, -103, -3321), name = ""},
	{pos = Vector3.new(-1716, -100, -3392), name = ""},
	{pos = Vector3.new(-950, -232, -2751), name = "Small Cave at Desolate Deep"},
	{pos = Vector3.new(-1155, -329, -4366), name = "Luminescent Cavern"},
	{pos = Vector3.new(-1161, -345, -4922), name = "Crimson Cavern"},
	{pos = Vector3.new(-934, -361, -4771), name = ""},
	{pos = Vector3.new(-5120, 158, -1629), name = "Scoria Reach"},
	{pos = Vector3.new(-5502, 153, -1962), name = ""},
	{pos = Vector3.new(-5219, 158, -1511), name = ""},
	{pos = Vector3.new(-4508, -699, -2027), name = ""},
	{pos = Vector3.new(15, 136, 1933), name = "Terrapin"},
	{pos = Vector3.new(4376, -2009, -4728), name = "Cultist Lair"},
	{pos = Vector3.new(4453, -2710, -4600), name = "The Sanctum"},
	{pos = Vector3.new(4376, -2706, -4749), name = ""},
	{pos = Vector3.new(-4061, -561, 1529), name = "Atlantis"},
	{pos = Vector3.new(-3552, -550, 924), name = "Poseidon Temple"},
	{pos = Vector3.new(-4231, -627, 2664), name = "Zeus Trial"},
	{pos = Vector3.new(-3952, -673, 2421), name = ""},
	{pos = Vector3.new(-5018, -589, 1762), name = "Sunken Depths"},
	{pos = Vector3.new(-9068, -2346, 1050), name = "Bellona's Frenzy of War"},
	{pos = Vector3.new(-8972, -2272, 150), name = ""},
	{pos = Vector3.new(-8560, -2881, 847), name = "Apollo's Song of Light"},
	{pos = Vector3.new(-8780, -2838, 786), name = ""},
	{pos = Vector3.new(-9084, -2799, 860), name = ""},
	{pos = Vector3.new(-8635, -3091, 504), name = "Poseidon's Storm of Floods"},
	{pos = Vector3.new(-8905, -3171, 464), name = ""},
	{pos = Vector3.new(-7638, -4242, 426), name = "Hades' Underworld"},
	{pos = Vector3.new(-8406, -4250, 148), name = ""},
	{pos = Vector3.new(-8279, -4252, 596), name = ""},
	{pos = Vector3.new(-8699, -4196, -521), name = "Olympian Fissure"},
	{pos = Vector3.new(-8685, -4243, -313), name = ""},
	{pos = Vector3.new(-8862, -4303, -892), name = ""},
	{pos = Vector3.new(-8904, -4300, -874), name = ""},
	{pos = Vector3.new(-2885, 142, -2258), name = "Lost Jungle"},
	{pos = Vector3.new(-2819, -286, -2431), name = "Toxic Grove"},
	{pos = Vector3.new(-2437, -267, -2557), name = ""},
	{pos = Vector3.new(-2584, -309, -3109), name = "Living Garden"},
	{pos = Vector3.new(-2570, -310, -2928), name = ""},
	{pos = Vector3.new(-1934, -302, -3349), name = "Nectar Den"},
	{pos = Vector3.new(-1885, 354, 198), name = "Roslit Volcano"},
	{pos = Vector3.new(-3393, -1974, 3887), name = "Volcanic Vents"},
	{pos = Vector3.new(-2941, -1954, 4252), name = ""},
	{pos = Vector3.new(-4418, -11167, 1595), name = "Calm Zone"},
	{pos = Vector3.new(-106, -566, 1578), name = "Vertigo"},
	{pos = Vector3.new(-87, -724, 1154), name = ""},
	{pos = Vector3.new(908, -620, 616), name = "Depths"},
	{pos = Vector3.new(1007, -596, 1212), name = ""},
	{pos = Vector3.new(1357, -614, 2357), name = "Crystal Cove"},
	{pos = Vector3.new(6026, 258, 589), name = "Ancient Isle"},
	{pos = Vector3.new(5944, 154, 453), name = ""},
	{pos = Vector3.new(-3105, -756, 1667), name = "Ancient Archives"},
	{pos = Vector3.new(-3222, -768, 1866), name = ""},
	{pos = Vector3.new(3038, -1102, 431), name = "Sunken Reliquary"},
	{pos = Vector3.new(4630, -1083, 835), name = "Inner Tidefall Castle"},
	{pos = Vector3.new(4311, -1086, 1045), name = ""},
	{pos = Vector3.new(2999, -1126, 2046), name = "Crowned Ruins"},
	{pos = Vector3.new(2383, -1011, 747), name = "Coral Bastion"},
	{pos = Vector3.new(20260, 273, 5596), name = "Overgrowth Caves"},
	{pos = Vector3.new(19862, 424, 5390), name = "Frigid Cavern"},
	{pos = Vector3.new(20016, 900, 5675), name = "Glacial Grotto"},
	{pos = Vector3.new(20067, 1226, 5413), name = ""},
	{pos = Vector3.new(21236, 617, 3561), name = "Boreal Pines"},
	{pos = Vector3.new(21779, 133, 3909.5), name = ""},
	{pos = Vector3.new(-711, -864, -9), name = "Mineshaft"},
	{pos = Vector3.new(-790, -812, -316), name = ""},
	{pos = Vector3.new(-265, -897, -99), name = ""},
	{pos = Vector3.new(1523, -802, -238), name = "Keepers Altar"},
	{pos = Vector3.new(790, -716, -14), name = ""},
	{pos = Vector3.new(567, 281, -2121), name = "Castaway Cliffs"},
	{pos = Vector3.new(285, 211, -2233), name = ""},
	{pos = Vector3.new(-2796, 208, 1542), name = "Forsaken Shores"},
	{pos = Vector3.new(2884, 136, 2705), name = "Snowcap"},
	{pos = Vector3.new(2794, 89, 2498), name = "Snowburrow"},
	{pos = Vector3.new(1821, -324, -2440), name = "Birch Cay"},
}

local total = #locations
local currentIndex = 1
local delayTime = 5
local isRunning = false
local isPaused = false
local tourThread = nil

-- ================== TELEPORT ==================
local function getRoot(char)
	return char:FindFirstChild("HumanoidRootPart")
		or char:FindFirstChild("UpperTorso")
		or char:FindFirstChild("Torso")
end

local function teleportTo(pos)
	local char = player.Character
	local root = char and getRoot(char)
	if root then
		root.CFrame = CFrame.new(pos)
	end
end

-- ================== GUI ==================
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "TPTourGUI"
screenGui.ResetOnSpawn = false
screenGui.Parent = player:WaitForChild("PlayerGui")

local main = Instance.new("Frame")
main.Size = UDim2.new(0, 280, 0, 320)
main.Position = UDim2.new(0.5, -140, 0.42, -160)
main.BackgroundColor3 = Color3.fromRGB(20, 20, 25)
main.BackgroundTransparency = 0.15
main.BorderSizePixel = 0
main.Parent = screenGui

local corner = Instance.new("UICorner")
corner.CornerRadius = UDim.new(0, 12)
corner.Parent = main

-- Title
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, -40, 0, 32)
title.Position = UDim2.new(0, 10, 0, 6)
title.BackgroundTransparency = 1
title.Text = "TP Tour (75 Locations)"
title.TextColor3 = Color3.fromRGB(0, 180, 255)
title.TextScaled = true
title.Font = Enum.Font.GothamBold
title.TextXAlignment = Enum.TextXAlignment.Left
title.Parent = main

-- Close Button
local closeBtn = Instance.new("TextButton")
closeBtn.Size = UDim2.new(0, 28, 0, 28)
closeBtn.Position = UDim2.new(1, -34, 0, 6)
closeBtn.BackgroundColor3 = Color3.fromRGB(180, 40, 40)
closeBtn.Text = "X"
closeBtn.TextColor3 = Color3.new(1,1,1)
closeBtn.TextScaled = true
closeBtn.Font = Enum.Font.GothamBold
closeBtn.Parent = main
local closeCorner = Instance.new("UICorner")
closeCorner.CornerRadius = UDim.new(0, 6)
closeCorner.Parent = closeBtn

closeBtn.MouseButton1Click:Connect(function()
	isRunning = false
	isPaused = false
	screenGui:Destroy()
end)

-- Progress
local progressLabel = Instance.new("TextLabel")
progressLabel.Size = UDim2.new(1, -20, 0, 28)
progressLabel.Position = UDim2.new(0, 10, 0, 42)
progressLabel.BackgroundTransparency = 1
progressLabel.Text = "Progress: 0 / " .. total
progressLabel.TextColor3 = Color3.fromRGB(0, 255, 140)
progressLabel.TextScaled = true
progressLabel.Font = Enum.Font.GothamBold
progressLabel.Parent = main

-- Current Location
local locationLabel = Instance.new("TextLabel")
locationLabel.Size = UDim2.new(1, -20, 0, 22)
locationLabel.Position = UDim2.new(0, 10, 0, 72)
locationLabel.BackgroundTransparency = 1
locationLabel.Text = "Ready"
locationLabel.TextColor3 = Color3.fromRGB(220, 220, 220)
locationLabel.TextScaled = true
locationLabel.Font = Enum.Font.Gotham
locationLabel.TextXAlignment = Enum.TextXAlignment.Left
locationLabel.Parent = main

-- Delay
local delayLabel = Instance.new("TextLabel")
delayLabel.Size = UDim2.new(0, 80, 0, 22)
delayLabel.Position = UDim2.new(0, 10, 0, 105)
delayLabel.BackgroundTransparency = 1
delayLabel.Text = "Delay (s):"
delayLabel.TextColor3 = Color3.fromRGB(200, 200, 200)
delayLabel.TextScaled = true
delayLabel.Font = Enum.Font.Gotham
delayLabel.TextXAlignment = Enum.TextXAlignment.Left
delayLabel.Parent = main

local delayBox = Instance.new("TextBox")
delayBox.Size = UDim2.new(0, 70, 0, 26)
delayBox.Position = UDim2.new(0, 95, 0, 103)
delayBox.BackgroundColor3 = Color3.fromRGB(40, 40, 50)
delayBox.Text = "5"
delayBox.TextColor3 = Color3.new(1,1,1)
delayBox.TextScaled = true
delayBox.Font = Enum.Font.Gotham
delayBox.ClearTextOnFocus = false
delayBox.Parent = main
local delayCorner = Instance.new("UICorner")
delayCorner.CornerRadius = UDim.new(0, 6)
delayCorner.Parent = delayBox

-- Jump to
local jumpLabel = Instance.new("TextLabel")
jumpLabel.Size = UDim2.new(0, 80, 0, 22)
jumpLabel.Position = UDim2.new(0, 10, 0, 140)
jumpLabel.BackgroundTransparency = 1
jumpLabel.Text = "Go to #:"
jumpLabel.TextColor3 = Color3.fromRGB(200, 200, 200)
jumpLabel.TextScaled = true
jumpLabel.Font = Enum.Font.Gotham
jumpLabel.TextXAlignment = Enum.TextXAlignment.Left
jumpLabel.Parent = main

local jumpBox = Instance.new("TextBox")
jumpBox.Size = UDim2.new(0, 70, 0, 26)
jumpBox.Position = UDim2.new(0, 95, 0, 138)
jumpBox.BackgroundColor3 = Color3.fromRGB(40, 40, 50)
jumpBox.Text = "1"
jumpBox.TextColor3 = Color3.new(1,1,1)
jumpBox.TextScaled = true
jumpBox.Font = Enum.Font.Gotham
jumpBox.ClearTextOnFocus = false
jumpBox.Parent = main
local jumpCorner = Instance.new("UICorner")
jumpCorner.CornerRadius = UDim.new(0, 6)
jumpCorner.Parent = jumpBox

local jumpBtn = Instance.new("TextButton")
jumpBtn.Size = UDim2.new(0, 70, 0, 26)
jumpBtn.Position = UDim2.new(0, 175, 0, 138)
jumpBtn.BackgroundColor3 = Color3.fromRGB(0, 120, 180)
jumpBtn.Text = "Go"
jumpBtn.TextColor3 = Color3.new(1,1,1)
jumpBtn.TextScaled = true
jumpBtn.Font = Enum.Font.GothamBold
jumpBtn.Parent = main
local jumpBtnCorner = Instance.new("UICorner")
jumpBtnCorner.CornerRadius = UDim.new(0, 6)
jumpBtnCorner.Parent = jumpBtn

-- Buttons
local function createBtn(text, posY, color)
	local btn = Instance.new("TextButton")
	btn.Size = UDim2.new(1, -20, 0, 34)
	btn.Position = UDim2.new(0, 10, 0, posY)
	btn.BackgroundColor3 = color
	btn.Text = text
	btn.TextColor3 = Color3.new(1,1,1)
	btn.TextScaled = true
	btn.Font = Enum.Font.GothamBold
	btn.Parent = main
	local c = Instance.new("UICorner")
	c.CornerRadius = UDim.new(0, 8)
	c.Parent = btn
	return btn
end

local startBtn = createBtn("START", 180, Color3.fromRGB(0, 150, 60))
local pauseBtn = createBtn("PAUSE", 220, Color3.fromRGB(180, 120, 0))
local resetBtn = createBtn("RESET", 260, Color3.fromRGB(140, 40, 40))

-- ================== LOGIC ==================
local function updateUI()
	progressLabel.Text = string.format("Progress: %d / %d", currentIndex - 1, total)
	
	if currentIndex > total then
		locationLabel.Text = "Selesai!"
		return
	end
	
	local loc = locations[currentIndex]
	if loc.name and loc.name ~= "" then
		locationLabel.Text = string.format("#%d - %s", currentIndex, loc.name)
	else
		locationLabel.Text = string.format("#%d", currentIndex)
	end
end

local function stopTour()
	isRunning = false
	isPaused = false
	if tourThread then
		task.cancel(tourThread)
		tourThread = nil
	end
	startBtn.Text = "START"
	startBtn.BackgroundColor3 = Color3.fromRGB(0, 150, 60)
	pauseBtn.Text = "PAUSE"
end

local function runTour()
	if tourThread then task.cancel(tourThread) end
	
	tourThread = task.spawn(function()
		while isRunning and currentIndex <= total do
			if isPaused then
				task.wait(0.2)
				continue
			end
			
			local loc = locations[currentIndex]
			teleportTo(loc.pos)
			updateUI()
			
			currentIndex += 1
			
			if currentIndex > total then
				locationLabel.Text = "Selesai! Semua lokasi sudah dikunjungi."
				progressLabel.Text = string.format("Progress: %d / %d", total, total)
				stopTour()
				break
			end
			
			-- Delay
			local waitTime = tonumber(delayBox.Text) or 5
			if waitTime < 0.5 then waitTime = 0.5 end
			task.wait(waitTime)
		end
	end)
end

startBtn.MouseButton1Click:Connect(function()
	if isRunning then return end
	
	isRunning = true
	isPaused = false
	startBtn.Text = "RUNNING..."
	startBtn.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
	pauseBtn.Text = "PAUSE"
	runTour()
end)

pauseBtn.MouseButton1Click:Connect(function()
	if not isRunning then return end
	
	isPaused = not isPaused
	if isPaused then
		pauseBtn.Text = "RESUME"
		pauseBtn.BackgroundColor3 = Color3.fromRGB(0, 140, 100)
	else
		pauseBtn.Text = "PAUSE"
		pauseBtn.BackgroundColor3 = Color3.fromRGB(180, 120, 0)
	end
end)

resetBtn.MouseButton1Click:Connect(function()
	stopTour()
	currentIndex = 1
	updateUI()
	locationLabel.Text = "Reset ke awal"
end)

jumpBtn.MouseButton1Click:Connect(function()
	local num = tonumber(jumpBox.Text)
	if num and num >= 1 and num <= total then
		stopTour()
		currentIndex = num
		updateUI()
		locationLabel.Text = "Siap lanjut dari #" .. num
	else
		locationLabel.Text = "Nomor tidak valid (1-" .. total .. ")"
	end
end)

-- Drag
local dragging = false
local dragStart, startPos

main.InputBegan:Connect(function(input)
	if input.UserInputType == Enum.UserInputType.MouseButton1 then
		dragging = true
		dragStart = input.Position
		startPos = main.Position
	end
end)

UserInputService.InputChanged:Connect(function(input)
	if dragging and input.UserInputType == Enum.UserInputType.MouseMovement then
		local delta = input.Position - dragStart
		main.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
	end
end)

UserInputService.InputEnded:Connect(function(input)
	if input.UserInputType == Enum.UserInputType.MouseButton1 then
		dragging = false
	end
end)

-- Init
updateUI()
print("Total lokasi:", total)
