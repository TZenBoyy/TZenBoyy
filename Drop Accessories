-- Parent this script to StarterPlayerScripts or StarterCharacterScripts

local player = game.Players.LocalPlayer

-- Function to drop all accessories
local function dropAccessories()
    local character = player.Character or player.CharacterAdded:Wait()

    for _, accessory in ipairs(character:GetChildren()) do
        if accessory:IsA("Accessory") then
            -- Detach the accessory from the character
            accessory.Parent = workspace
            accessory.Handle.CFrame = character.HumanoidRootPart.CFrame + Vector3.new(0, 5, 0)
        end
    end
end

-- Run the function when the player character loads
player.CharacterAdded:Connect(function()
    dropAccessories()
end)

-- Drop accessories for the current character if it's already loaded
if player.Character then
    dropAccessories()
end
