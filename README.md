minestat
========

A Minecraft server status checker

# Below is an example using the MineStat class.
# If server is offline, other instance members will be nil.
ms = MineStat.new("cubekingdom.net", 25565)
puts "Minecraft server status of #{ms.hostname} on port #{ms.port}:"
if ms.online
  puts "Server is online running version #{ms.version} with #{ms.current_players} out of #{ms.max_players} players."
  puts "Message of the day: #{ms.motd}"
else
  puts "Server is offline!"
end
