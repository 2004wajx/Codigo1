{{exec "remind" "2m45s" "__**Patata a minar!**__ ⛏"}}
{{ $avatar := (joinStr "" "https://cdn.discordapp.com/avatars/" (toString .User.ID) "/" .User.Avatar ".png") }}
{{ $embed := cembed
 "title" "⏰ Recordatorio Activado"
"description" "**🔔 En** `2m45s` **te recuerdo usar** `!mine`" 
"color" 4645612 
"author" (sdict "name" "Potatio y sus Patatas Fritas🍟" "url" "https://www.youtube.com/c/PotatioYT" "icon_url" "https://images-ext-2.discordapp.net/external/BVlN6bbXizWYkTvUPCv8lOK986SRPKSHcKoemRNhFeA/https/cdn.discordapp.com/icons/325393764141236224/f724b7cd309597835bb4adc0facc9544.png") 
    "thumbnail" (sdict "url" $avatar) 
    "footer" (sdict "text" "Recuerda usar vida ❤️" "icon_url" "https://emoji.gg/assets/emoji/4794_Kanna_Nom_Ping.gif") 
    "timestamp" .Message.Timestamp
}}
{{sendMessage nil $embed}}
{{deleteResponse 0}}
