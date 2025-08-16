local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local enabled = true
local himabyssstartslam = false
local himabysswarning = 0
local function HighlightPrt(inst)
    if inst:IsA('BasePart') then
        inst.Transparency = 0
        if not inst:FindFirstChild('Highlight') then
            Instance.new('Highlight', inst)
        end
        if inst:FindFirstChild('BillboardGui') then
            inst.BillboardGui.AlwaysOnTop = true
        end
        if inst:FindFirstChild('VisualEffects') then
            for i, v in pairs(inst.VisualEffects:GetDescendants()) do
                if v:IsA('BillboardGui') then
                    v.AlwaysOnTop = true
                end
            end
        end
        if inst:FindFirstChild('GOKU') then
            if inst:FindFirstChild('Attachment') then
                inst.Attachment:Destroy()
            end
            if inst:FindFirstChild('PointLight') then
                inst.PointLight:Destroy()
            end
        end
        if not inst:FindFirstChild('CoolEsp') then
            local esptxt = Instance.new('BillboardGui', inst)
            esptxt.Name = 'CoolEsp'
            esptxt.AlwaysOnTop = true
            esptxt.Size = UDim2.new(10, 0, 10, 0)
            esptxt.StudsOffset = Vector3.new(0, 7, 0)
            local txtlabel = Instance.new('TextLabel', esptxt)
            txtlabel.Size = UDim2.new(1, 0, 1, 0)
            txtlabel.TextColor3 = Color3.new(1, 1, 1)
            txtlabel.TextStrokeColor3 = Color3.new(0, 0, 0)
            txtlabel.TextStrokeTransparency = 0
            txtlabel.TextScaled = true
            txtlabel.Text = inst.Name
            txtlabel.BackgroundTransparency = 1
        end
    end
    if inst:FindFirstChild('CoolEsp') then
        if inst:FindFirstChild('Attachment') then
            if inst:FindFirstChild('Attachment'):FindFirstChild('Arrow') then
                if
                    inst:FindFirstChild('Attachment')
                        :FindFirstChild('Arrow').Enabled
                    == true
                then
                    inst.CoolEsp.TextLabel.Text = inst.Name
                        .. ' - '
                        .. 'Going To Dash'
                else
                    inst.CoolEsp.TextLabel.Text = inst.Name
                end
            end
        end
        if inst:FindFirstChild('HealthAlterWarning') then
            inst.CoolEsp.TextLabel.Text = inst.Name .. ' - ' .. 'Slam Warning'
        elseif inst.Name == 'him abyss' then
            inst.CoolEsp.TextLabel.Text = inst.Name
        end
    end
end

local Window = Rayfield:CreateWindow({
    Name = 'Tons Of Chases',
    Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
    LoadingTitle = 'cool hub',
    LoadingSubtitle = 'by meh',
    ShowText = 'Rayfield', -- for mobile users to unhide rayfield, change if you'd like
    Theme = 'Default', -- Check https://docs.sirius.menu/rayfield/configuration/themes

    ToggleUIKeybind = Enum.KeyCode.RightShift, -- The keybind to toggle the UI visibility (string like "K" or Enum.KeyCode)

    DisableRayfieldPrompts = false,
    DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

    ConfigurationSaving = {
        Enabled = false,
        FolderName = 'CoolHub', -- Create a custom folder for your hub/game
        FileName = 'Tons of chases',
    },

    Discord = {
        Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
        Invite = 'noinvitelink', -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ ABCD would be ABCD
        RememberJoins = true, -- Set this to false to make them join the discord every time they load it up
    },

    KeySystem = false, -- Set this to true to use our key system
    KeySettings = {
        Title = 'Untitled',
        Subtitle = 'Key System',
        Note = 'No method of obtaining the key is provided', -- Use this to tell the user how to get a key
        FileName = 'Key', -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
        SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
        GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
        Key = { 'Hello' }, -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
    },
})

local SublevelTab = Window:CreateTab('Sublevel', 'route')

local FakeWalls = SublevelTab:CreateToggle({
    Name = 'Show Fake/Wraith Walls',
    CurrentValue = false,
    Flag = 'wraithwalls',
    Callback = function(Value)
        getgenv().ShowRFakes = Value
    end,
})

local VisualsTab = Window:CreateTab('Visuals', 'eye')
local ChaserESP = VisualsTab:CreateToggle({
    Name = 'Chaser ESP',
    CurrentValue = false,
    Flag = 'chaseresp',
    Callback = function(Value)
        getgenv().espchaserthing = Value
    end,
})

local MiscTab = Window:CreateTab('Misc', 'cake-slice')

local destroyButton = MiscTab:CreateButton({
    Name = 'Destroy UI',
    Callback = function()
        enabled = false
        getgenv().ShowRFakes = false
        getgenv().espchaserthing = false
        Rayfield:Destroy()
    end,
})
while enabled == true do
    if getgenv().ShowRFakes then
    if workspace.Sublevel:FindFirstChild("Walls") then
        if not workspace.Sublevel.Walls:FindFirstChild('HeresyWall') then
            for i, v in pairs(workspace.Sublevel:GetDescendants()) do
                if v.Parent ~= nil then
                    if
                        v.Name == 'WraithGate'
                        or v.Name == 'WraithGate2'
                        or v.Name == 'Block'
                    then
                        v.Transparency = 0.5
                    end
                    if
                        (
                            v.Parent.Name == 'RemoveWall'
                            or v.Parent.Name == 'UncollideWall'
                            or v.Parent.Name == 'InvertedRemoveWall'
                            or v.Parent.Name == 'InvertInterruptAndRemoveWall'
                            or v.Parent.Name == 'InterruptnRemoveWall'
                            or v.Parent.Name == 'InvertRemoveWall'
                            or v.Parent.Name == 'PurpleInterruptandRemoveWall'
                            or v.Parent.Name == 'PurpleRemoveWall'
                            or v.Parent.Name == 'InvertRemoveWall'
                            or v.Parent.Name == 'DoubleInterruptInvertInterruptandRemoveWall'
                            or v.Parent.Name == ''
                        )
                        and (
                            v:IsA('BasePart')
                            and v.Name ~= 'TriggerPart'
                            and v.Name ~= 'WraithGate'
                            and v.Name ~= 'WraithGate2'
                        )
                    then
                        v.Transparency = 0.9
                        for i, v2 in pairs(v:GetChildren()) do
                            if v2:IsA('Texture') then
                                v2.Transparency = 0.9
                            end
                        end
                    end
                    if
                        v.Parent.Name == 'InterruptWall'
                        and v.Name ~= 'WraithGate'
                        and v.Name ~= 'Function'
                        and v.Name ~= 'TriggerPart'
                    then
                        v.Transparency = 0.9
                    end
                    if v.Name == 'FAKEGOKU' then
                        v.Transparency = 0.9
                        for i, v2 in pairs(v:GetChildren()) do
                            v2.Transparency = 1
                        end
                    end
                    if v:IsA('BasePart') then
                        if
                            v.CanCollide == false
                            and v.Name ~= 'TriggerPart'
                            and v.Name ~= 'Trigger'
                        then
                            v.Transparency = 0.9
                            for i, v2 in pairs(v:GetChildren()) do
                                if v2:IsA('Texture') then
                                    v2.Transparency = 0.9
                                end
                            end
                        end
                        if
                            v.Anchored == false
                            and v.Name ~= 'TriggerPart'
                            and v.Name ~= 'Trigger'
                        then
                            v.Transparency = 0.9
                            for i, v2 in pairs(v:GetChildren()) do
                                if v2:IsA('Texture') then
                                    v2.Transparency = 0.9
                                end
                            end
                        end
                    end
                end
            end
        end
    end
    end
    if getgenv().espchaserthing == true then
        for i, v in pairs(workspace.Chasers:GetChildren()) do
            HighlightPrt(v)
        end
        for i, v in pairs(workspace:GetChildren()) do
            if v:FindFirstChild('TheSmiler') or v:FindFirstChild('Kill') then
                HighlightPrt(v)
            end
        end
        task.wait(0.5)
    end
    task.wait(0.5)
end
