local HumValues = {}
local LP = game:GetService('Players').LocalPlayer
local LC = LP.Character
local LB = LP.Backpack
local Hum = LC.Humanoid
local Head = LC:FindFirstChild('Head')
local Mesh = Head:FindFirstChild('Mesh')
Head.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0, 0, 0)

if not LC or not Hum or not Head or not Mesh or not Hum:FindFirstChildWhichIsA('NumberValue') or not Mesh:FindFirstChild('OriginalSize') then
    return
end

for _, v in next, Hum:GetChildren() do
    if v:IsA('NumberValue') then
        table.insert(HumValues, v)
    end
end

for i = 1, #HumValues do
    Mesh:WaitForChild('OriginalSize')
    for _, v in next, Mesh:GetChildren() do
        if v:IsA('Vector3Value') and v.Name == 'OriginalSize' then
            v:Destroy()
        end
    end
    Head:WaitForChild('OriginalSize')
    for _, v in next, Head:GetChildren() do
        if v:IsA('Vector3Value') and v.Name == 'OriginalSize' then
            v:Destroy()
        end
    end
    HumValues[i]:Destroy()
    wait(.2)
end
Head.CanCollide = false
Hum.HipHeight = 16
