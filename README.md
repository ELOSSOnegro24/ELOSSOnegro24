const Discord = require("discord.js");
const client = new Discord.Client();
const DabiImages = require("dabi-images");
const nsfw = require("discord-simple-nsfw");
const akaneko = require("akaneko");
const pet = require("pet-pet-gif");

function presence() {
	client.user.setPresence({
		status: 'online',
		activity: {
			name: `_help`,
			type: 'PLAYING'

		}
	});
}

client.on("ready", () => {
	console.log("wenas");
	presence();
});

client.on('message', async message => {
	console.log(message.content)

	if (message.content === '_help') {
		const embed = new Discord.MessageEmbed()
			.setTitle(`Estos son mis comandos`)
.setDescription(`:video_game: **Comandos de juegos** :video_game:\n\n*ESTOS COMANDOS SIRVEN RESPONIENDO UN MENSAGE DE LA PERSONA QUE QUIERES QUE NOMBRE EL BOT*\n\n➪ impostor **|** eres o no eres el impostor\n➪ test **|** vamos a ver si tienes covit\n➪ gift **|** adale algo a alguien\n➪ amor **|** q tan complative somos??\n➪ susto **|** porq asustas we\n➪ducha **|** q quieres bañar??\n➪ lindometro **|** que tan lindo eres\n➪ perfil **|** muestro tu foto de perfil\n\n:teddy_bear: **+ Comandos** :teddy_bear:\n➪ ae **|** ...\n➪ habla **|** quieres hablar con migo??\n➪ dep **|**te digo cosas de mi\n➪ obligame **|** obligame prro\n➪ meme **|** quieres reirte??\n➪ moneda **|** apostamos??\n➪ pat **|** te muestro un gif\n➪ xf **|** que es xf\n➪ prefix **|** ...\n➪ ª **|** descubre q sale\n\n:underage: **Comandos NSFW** :underage:\n➪ p **|** solo para +18\n➪ neko **|** quieres ver una waifu??\n➪ no antojes **|** te mustro una foto de no antojar\n\n:sunglasses: **Comandos sin prefix** :sunglasses:\n➪ messirve **|** a mi tambien\n➪ nomessirve **|** a mi tampoco me sirve xf\n➪ no pos pio **|** pio\n➪ a **|** pos a\n➪ me umillo **|** nos umillo\n\n:mobile_phone: **Gits** :mobile_phone:\n➪ sat **|** no te pongas triste\n➪ run **|** de quien corres\n\n:beginner: **Otros** :beginner:\n➪ invit **|** invitame a tu server\n➪ creador **|** te cuento cosas de mi creador\n➪ info **|** te doy la infomasion de un miembro\n➪ serverinfo **|** muestro la informasion de tu servidor`)
			.setImage('https://images-ext-2.discordapp.net/external/-14msrjJiArDjldv72CiU9Rf2Wuzi0PcDKxqd26eF38/%3Fwidth%3D400%26height%3D133/https/images-ext-1.discordapp.net/external/AxqI-ylJtpcIBnlEAR2CSTM7rwrRh9USQYKDqNxgFaQ/https/media.discordapp.net/attachments/842575490959147049/858111198361026580/banner.png')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_prefix') {
		const embed = new Discord.MessageEmbed()
			.setDescription('**valla creo que as decubirto mi prefix y me temo que te tengo que entiesar**')
			.setImage('https://images-ext-2.discordapp.net/external/emoBjDLe5VseNIv1o_2iQalBBsqu6n0m91urcNIshS8/%3Fv%3D1/https/cdn.discordapp.com/emojis/826530802187239424.png')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_creador') {
		const embed = new Discord.MessageEmbed()
			.setTitle('El es mi creador y sus redes sociales')
			.setImage(`https://media.discordapp.net/attachments/842575490959147049/858111198361026580/banner.png`)
			.setDescription('**Creador:**\nEL OSSO negro_24#5657\n\n**Canal de youtube:** https://www.youtube.com/channel/UCcR6_M4fSmg5vsZcKTKqL5w\n\n**Server de discord:**\n https://discord.gg/T5zQxxGuJH%27%27\n\n**De donde es pues de:\n\n:sunglasses: MEXIOSSO** :sunglasses:')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_xf') {
		const embed = new Discord.MessageEmbed()
			.setTitle('Que es xf')
			.setDescription('**NO PUEDES USAR ESTE COMANDO:**  _xf\n*OK NO PERO TE CONTARE LA HISTORIA DEL "XF"*\ncres q XF fue un error pues tienes la razon XF fue un error pero se usa para desir q algo es divertido y a la ves triste\n\n**Ejemplo:**\n:smiling_face_with_tear: como ella no te ama xf :smiling_face_with_tear:')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_dep') {
		const embed = new Discord.MessageEmbed()
			.setDescription(':smiling_face_with_tear: Soy bot que ase cosas y no se que hago vivo xd :smiling_face_with_tear:')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_ae') {
		const embed = new Discord.MessageEmbed()
			.setDescription('**no pos no se q es ae XD**')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_invit') {
		const embed = new Discord.MessageEmbed()
			.setTitle('Invitame a tu server')
			.setDescription('https://discord.com/api/oauth2/authorize?client_id=854572375482957844&permissions=8&scope=bot')
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_lindometro') {
		let numero = Math.floor(Math.random() * 100)
		let user = message.mentions.users.first() || message.author
		let emoji = "";
		if (numero < 30) {
			emoji = ':face_vomiting:';
		} else if (numero < 40) {
			emoji = ':neutral_face:';
		} else if (numero < 70) {
			emoji = ':open_mouth:';
		} else if (numero < 95) {
			emoji = ':heart_eyes:';
		} else if (numero < 101) {
			emoji = ':heart_eyes: :smiling_face_with_3_hearts: :kissing_heart: :yum: :hot_face: :smiling_imp: :sweat_drops: :eggplant:';
		}
		const embed = new Discord.MessageEmbed()
			.setTitle('Segun yo:')
			.setDescription(`El porcentaje de lindura de **${user.username}** es de un **${numero}%** ${emoji}`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_ducha') {
		let user = message.mentions.users.first() || message.author
		if (!user) return message.channel.send("No es un secreto que no te bañas. Menciona a Alguien")
		var bañado = Math.floor(Math.random() * 70);
		var olor = ["mal", "horrible", "pesimo", "super bien", "bien", "mejor que otros dias",
			"como colonia de bebe", "mas o menos", "taaaaaaaaaaaannnnnnnnn maaaaaaaaaaaal *cmuere*",
			"excelente", "como lavanda", "como aliento de dragon", "taaaaaaaan bieeeen *cmuere*", "como a cebolla", "como si no se hubiera bañado para nada"];
		var aleatorio = Math.floor(Math.random() * (olor.length));
		const embed = new Discord.MessageEmbed()
			.setDescription(`**${user.username}** se baña ${bañado} veces al mes pero huele ${olor[aleatorio]}`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === `_ª`) {
		const embed = new Discord.MessageEmbed()
			.setTitle('porq me insultas we  >:(')
			.setImage(`https://media.discordapp.net/attachments/844398019888676907/854575921801330688/unknown.png`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === `_amor`) {
		let users = message.mentions.users.first();
		if (!users) return message.reply("Menciona a alguien porfavor!")
		if (users === client.user) return message.channel.send("**NO puedo yo tengo a alguien mas!**")
		const random = Math.floor(Math.random() * 100);
		let heard = "";
		if (random < 50) {
			heard = ':broken_heart:';
		} else if (random < 80) {
			heard = ':sparkling_heart: ';
		} else if (random < 101) {
			heard = ':heart:';
		}
		let resp = [`El porcetanje de ${message.author.username} & ${users.username} son:`, `valla yo calculo que ${message.author.username} & ${users.username} da a:`]
		let msg = resp[Math.floor(Math.random() * resp.length)]
		const embed = new Discord.MessageEmbed()
			.setAuthor(`${msg}`)
			.setDescription(`${heard} ${random} %${heard}`)
			.setColor(`#000000`)
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if(message.content === `_perfil`) {
if(message.author.bot) return;
let miembro = message.mentions.users.first()  
if (!miembro) {
const embed = new Discord.MessageEmbed()
    .setTitle('Tu perfil es:')
    .setImage(`${message.author.displayAvatarURL({dynamic: true, size : 1024 })}`)
    .setColor(`#000000`)
    .setFooter(`bot en face beta`);
message.channel.send(embed);
} else {
const embed = new Discord.MessageEmbed()
    .setTitle('Su perfil es:')
    .setImage(`${miembro.displayAvatarURL({dynamic: true, size : 1024 })}`)
    .setColor(`#000000`)
    .setFooter(`bot en fase beta`);
message.channel.send(embed);
}
}

	if (message.content === `_p`) {
		const DabiClient = new DabiImages.Client()
		DabiClient.nsfw.real.ass()
			.then((res) => {
				console.log('RES:', res.url)
				message.channel.send(res.url)
			})
	}

	if (message.content === `_neko`) {
		let neko = await akaneko.neko();
		const embed = new Discord.MessageEmbed()
			.setTitle(`No antojes wey`)
			.setImage(`${neko}`)
			.setColor("#000000")
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === `messirve`) {
		const embed = new Discord.MessageEmbed()
		  .setTitle(`x2`)
			.setImage(`https://cdn.discordapp.com/emojis/835306161254957077.png?v=1`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === '_chiste') {
		const random = require('chistes-aleatorios');
		const chiste = await random.chistes();
		message.channel.send(chiste);
	}

if (message.content === `nomessirve`) {
		const embed = new Discord.MessageEmbed()
			.setTitle('x2')
			.setImage(`https://media.discordapp.net/attachments/835266125524369478/858179391774785536/nomessirve-messirve.gif`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

	if (message.content === `no pos pio`) {
		const embed = new Discord.MessageEmbed()
			.setTitle('x2')
			.setImage(`https://media.discordapp.net/attachments/835266125524369478/858181341203529774/186486196_281331067020244_603712608392665459_n.jpg`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

if (message.content === '_moneda') {
	  var moneda = Math.floor(Math.random() * 10);
  	var olo = [`**cara**`,`**cruz**`];
		var aleatori = Math.floor(Math.random() * (olo.length));
    const embed = new Discord.MessageEmbed()
      .setTitle('Lazar Moneda')
      .setDescription(`salio ${olo [aleatori]}`)
      .setColor('#000000')
			.setFooter(`${message.author.displayAvatarURL()}`)
      .setFooter('bot en fase beta | codigo hecho por Epilepsis#0364 y adaptado por mi')
message.channel.send(embed);
}

if (message.content === '_habla') {
	let user = message.mentions.users.first() || message.author
	let chistes = ['tu mama', 'ae', 'xf', 'tu papá es hombre', 'sigue asi wey y te entieso', 'ella no te ama', '7u7', 'que chamucos', 'XD', 'messirve', 'wevos', 'alv', 'que chingados wey es una buena idea', 'pito,pito doble,pito cosmico','f',''];
       let randomChiste = chistes[Math.floor(Math.random() * chistes.length)];
       const aceptenmeloplis = new Discord.MessageEmbed()
			 .setTitle('hablamos??')
       .setDescription(`${randomChiste}`)
       .setColor('#000000')
			 .setFooter('bot en fase beta')
message.channel.send(aceptenmeloplis);
}

if (message.content === `_mide`){
let usuario = message.mentions.users.first()
  let autor = message.author
  
  let decimal = Math.random() * 100 + 1;
  let numero = Math.floor(decimal);
  if(!usuario){
    const embed = new Discord.MessageEmbed()
      .setDescription(`La Berenjena de **${autor.username}** mide ${numero} centímetros`)
      .setFooter(message.author.tag, message.author.displayAvatarURL())
      .setColor('#00000')
    message.channel.send(embed)
  }else{
    if(usuario == client.user) return message.channel.send('**Si lo supieras te daria arimones siempre 7u7**')
    if(usuario.bot) return message.channel.send('**WEY no, queno ves q no tiene!**')
    const embed = new Discord.MessageEmbed()
		  .setTitle(`aver cuanto te mide`)
      .setDescription(`La Berenjena de ${usuario.username} mide ${numero} centímetros`)
      .setFooter(usuario.tag, usuario.displayAvatarURL())
      .setColor('#000000')
    message.channel.send(embed)  
  }
}

if (message.content === `_info`) {
let estados = {
      "online": "🟢 En Línea",
      "idle": "🟠 Ausente",
      "dnd": "🔴 No molestar",
      "offline": "⚫️ Desconectado/invisible"
    };

    const member = message.mentions.members.first() || message.member
    function formatDate (template, date) {
      var specs = 'YYYY:MM:DD:HH:mm:ss'.split(':')
      date = new Date(date || Date.now() - new Date().getTimezoneOffset() * 6e4)
      return date.toISOString().split(/[-:.TZ]/).reduce(function (template, item, i) {
        return template.split(specs[i]).join(item)
      }, template)
    }

    let badges1 = {
        
      'EARLY_SUPPORTER': '<:Earlysupporter:746029762274656317>',
      'DISCORD_EMPLOYEE': '<:Discordstaff:746029762513862666>',
      'DISCORD_PARTNER': '<:Discordpartner:746029762564194355>',
      'HYPESQUAD_EVENTS': '<:HypesquadEvents:746029762497085550>',
      'HOUSE_BRAVERY': '<:Houseofbravery:746029762459467858>',
      'HOUSE_BRILLIANCE': '<:Houseofbrilliance:746029762610331668>',
      'BUGHUNTER_LEVEL_1': '<:Bughunter:746029762522120203>',
      'BUGHUNTER_LEVEL_2': '<:Goldbughunter:746029762526576691>',
      'VERIFIED_DEVELOPER': '<:VerifiedBotDeveloper:746029762194964590>',
      'HOUSE_BALANCE': '<:Houseofbalance:746029762610331658>',
      'VERIFIED_BOT': '<:verified:753442204541911081>',
    }


    let obj = {
    "HOUSE_BRAVERY" : "Bravery" , "VERIFIED_BOT" : "Bot verificado" , "VWERIFIED_DEVELOPER" : "Desarrollador de bots verificado" , "HOUSE_BRILLIANCE" : "Brilliance" , "DISCORD_PARTNER" : "Socio de discord"
    }
    const embed = new Discord.MessageEmbed()
        .setColor("#000000")
        .setDescription("**INFORMACIÓN DEL USUARIO:**")
        .addField("**🎫 Nombre**:", "**" + `${member.user.tag}` + "**")
        .addField("**🎟 ID**:", `${member.user.id}` )
        .addField("**📌 Apodo del usuario**:", `${member.nickname !== null ? `${member.nickname}` : 'Ninguno'}`, true)
        .addField("**🛎 Fecha de Ingreso al Servidor:**", formatDate('DD/MM/YYYY, a las HH:mm:ss', member.joinedAt))
        .addField("**📥 Cuenta Creada:**", formatDate('DD/MM/YYYY, a las HH:mm:ss', member.user.createdAt))
        .addField("**🏳️ Insignias:**", member.user.flags.toArray().length ? member.user.flags.toArray().map(badge => badges1[badge]).join(' ') : "No tengo badges")
        .addField("**🎮  Jugando**:", member.user.presence.game != null ? user.presence.game.name : "Nada", true)
        .addField("**🎖 Roles:**", member.roles.cache.map(roles => `\`${roles.name}\``).join(', '))
        .addField("**🎨 Estado**:", "**" + estados[member.user.presence.status] + "**")
        .addField("**🚀 ¿Boostea?**:", member.premiumSince ? '**Estoy boosteando <a:boostingtop:755576533430698084>**' : '**No estoy boosteando**')
        .setThumbnail (member.user.displayAvatarURL({ format: "png", dynamic: true, size: 1024 }))
        .setFooter(`${message.author.username}`, `${message.author.displayAvatarURL()}`)
				.setFooter('bot en fase beta')
     message.channel.send(embed);
}

if (message.content === `_impostor`) {
const mencionado = message.mentions.members.first() 
let random = [
"No era el impostor",
"Era el impostor"
]
if(!mencionado)
 return message.channel.send(`. 　　　。　　　　•　 　ﾟ　　。 　　.

　　　.　　　 　　.　　　　　。　　 。　. 　

.　　 。　　　　　 ඞ 。 . 　　 • 　　　　•

　　ﾟ　　 ${message.author.username} ${random[Math.floor(Math.random() * random.length)]} 　 。　.

　　'　　　 ${Math.floor(Math.random() * 3) + 1} Impostores restantes 　 　　。

　　ﾟ　　　.　　　. ,　　　　.　 .`) 
message.channel.send(`. 　　　。　　　　•　 　ﾟ　　。 　　.

　　　.　　　 　　.　　　　　。　　 。　. 　

.　　 。　　　　　 ඞ 。 . 　　 • 　　　　•

　　ﾟ　　 **${mencionado.user.username}** ${random[Math.floor(Math.random() * random.length)]} 　 。　.

　　'　　　 ${Math.floor(Math.random() * 3) + 1} Impostores restantes 　 　　。

　　ﾟ　　　.　　　. ,　　　　.　 .`)
}

if (message.content === '_test') {
let rpts = [":warning: **A dado positivo al test de coronavirus!** :warning: ", ":partying_face: **A dado negativo al test de coronavirus!** :partying_face: "]
  let mencionado = message.mentions.users.first() || message.author
  const embedDatos = new Discord.MessageEmbed()
    .setTitle(`El resultado test de ${mencionado.username} :`)
		.setFooter('bot en fase beta')
    .setDescription(rpts[Math.floor(Math.random() * rpts.length)]);
    message.channel.send({ embed: embedDatos });
  }

if (message.content === `a`) {
		const embed = new Discord.MessageEmbed()
			.setImage(`https://cdn.discordapp.com/emojis/821395817634070588.gif?v=1`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

if (message.content === `_run`) {
		const embed = new Discord.MessageEmbed()
		  .setTitle(`corre de algo o de alguien`)
			.setImage(`https://cdn.discordapp.com/emojis/852783347846873089.gif?v=1`)
			.setColor('#000000')
			.setFooter('bot en fase beta')
		message.channel.send(embed);
	}

if (message.content.startsWith('_serverinfo')) {
var server = message.guild;
const embed = new Discord.MessageEmbed()
.setTitle("**SERVERINFO**")
.setDescription("**INFORMACION ACTUAL DEL SERVIDOR**")
.setThumbnail(server.iconURL())
.setAuthor(server.name, server.iconURL())
.addField('**FECHA DE CREACION**',`${server.joinedAt}`)
.addField(":rainbow_flag: **REGION:** :rainbow_flag:", message.guild.region)
.addField(":sunglasses: **OWNER DEL SERVIDOR:** :sunglasses:",`${server.owner.user}`)
.addField("** ID DEL OWNER :**",`${server.ownerID}`)
.addField(` :tv:**CANALES** [${server.channels.cache.size}]:tv:ㅤㅤ`, `Categoria: ${server.channels.cache.filter(x => x.type === "category").size} texto: ${server.channels.cache.filter(x => x.type === "text").size} voz: ${server.channels.cache.filter(x => x.type === "voice").size}`, true)
.addField(':upside_down: **MIEMBROS** :upside_down:', server.memberCount, true)
.addField(":robot: **BOTS** :robot:",`${message.guild.members.cache.filter(m => m.user.bot).size}`)
.addField('**EMOJIS**',message.guild.emojis.cache.size)
.addField('**BOOSTER**',message.guild.premiumSubscriptionCount.toString())
.addField(':lock: **NIVEL DE VERIFICACION** :lock:',`${server.verificationLevel}`)
.addField('**ROLES**', server.roles.cache.size,true)
.setColor("#000000")
message.channel.send(embed);
}

if (message.content === `_pat`) {
    let animatedGif = await pet(message.author.displayAvatarURL({format: "png"}))
		const petpet = new Discord.MessageAttachment(animatedGif, "petpet.gif") 
    message.channel.send(petpet)
		}

if (message.content === `_sat`) {
	let user = message.author
	let gifs = ['http://www.reactiongifs.com/r/sdtrs.gif', 'http://www.reactiongifs.com/r/spg.gif', 'https://images-ext-2.discordapp.net/external/s48-0u_HARHmVpjcMbFBOAiJsqlrWl94zc4QcRmipG4/https/c.tenor.com/qYbrL0rUVxgAAAAM/cute-animals.gif']
let randomIMG = gifs[Math.floor(Math.random() * gifs.length)]
const embed = new Discord.MessageEmbed()
    .setTitle(`${user.username} se puso sat`)
    .setImage(randomIMG)
    .setColor("BLACK")
message.channel.send(embed);
}

if (message.content === '_BLESS') {
		let mencionado = message.mentions.users.first() || message.author
	const embed = new Discord.MessageEmbed()
    .setTitle(`BLESS por ${mencionado.username}`)
    .setImage('https://cdn.discordapp.com/emojis/832712636600811521.png?v=1')
    .setColor("BLACK")
message.channel.send(embed);
}

if(message.content === '_susto'){
  const marsnpm = require("marsnpm");
 let user = message.mentions.users.first() || message.author;
let avatar = user.displayAvatarURL({dynamic: false, format: 'png', size: 2048})
let imagen = await marsnpm.susto(avatar);
let susto = new Discord.MessageAttachment(imagen, "susto.png")
message.channel.send(susto);
}

if(message.content === "no antojes") {
	let imagen =['https://media.discordapp.net/attachments/858070356593737750/859236509357834260/179226740_814122599522245_2255200871074487118_n.jpg']
let random = imagen[Math.floor(Math.random() * imagen.length)]
const embed = new Discord.MessageEmbed()
    .setDescription(`**WEY DEJA DE ANTOJAR**`)
    .setImage(random)
    .setColor("BLACK")
message.channel.send(embed);
}

if (message.content === '_meme') {
const karit = require('ckarit')
    let meme = await karit.meme()
    let embed = new Discord.MessageEmbed()
    .setImage(meme);
    message.channel.send(embed)
  }

if (message.content === 'me umillo') {	
    const embed = new Discord.MessageEmbed()
      .setTitle('NOS umillo')
      .setImage('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRhlaQO3yl7nK4D3WZ2W5yqfiFGCID5m0um8ubx1YCP4S56KbPACIEy0Tlbl7kB-NiBsoA&usqp=CAU')
      .setColor('#000000')
      .setFooter('bot en fase beta')
message.channel.send(embed);
}

if (message.content === 'dream') {
	const embed = new Discord.MessageEmbed()
      .setTitle('ESTE ES TU IDOLO??')
      .setImage('https://media.discordapp.net/attachments/817231388038004747/859922923463639071/tumblr_1ae94d5926c88ce32467e0f0a4941af5_c46e8b29_500.gif?width=427&height=427')
      .setColor('#000000')
      .setFooter('bot en fase beta')
message.channel.send(embed);
}

if (message.content === '_gift') {
	let usuario = message.mentions.users.first()
	if (!usuario) return message.reply("Menciona a alguien porfavor!")
  let autor = message.author
	let chistes = ["dinero :dollar:", 'clorox :battery:', 'una PC :computer:', 'UN CHINGO DE :moneybag:', 'mi hermano :teddy_bear:', 'un pastel :cake:', 'kk :poop:', 'su amistad :sparkling_heart: '];
       let randomChiste = chistes[Math.floor(Math.random() * chistes.length)];
       const aceptenmeloplis = new Discord.MessageEmbed()
       .setDescription(` **${autor.username}** le dio ${randomChiste} a **${usuario.username}**`)
       .setColor('#000000')
			 .setFooter('bot en fase beta')
message.channel.send(aceptenmeloplis);
  }

if (message.content === '_SONIC') {
	let gifs = ['https://images-ext-2.discordapp.net/external/zKwYvTXm-88kicgvSGESnhIkHo8eh14PTD2Ud5Wf_go/https/c.tenor.com/Utll2VF5lKEAAAAM/short-version-discord-friendly.gif', 'https://images-ext-2.discordapp.net/external/qOZmwIq7FP70rHB-LBodWwN8k6uty7SEGxf8SoQM6so/https/c.tenor.com/dWzbaStlrGIAAAAM/sonic-im-waiting.gif']
let randomIMG = gifs[Math.floor(Math.random() * gifs.length)]
const embed = new Discord.MessageEmbed()
    .setImage(randomIMG)
    .setColor("BLACK")
message.channel.send(embed);
}

if (message.content === '._:') {
	const embed = new Discord.MessageEmbed()
      .setTitle('._:')
      .setImage('https://media.discordapp.net/attachments/858070356593737750/860261688163172402/Z.png')
      .setColor('#000000')
      .setFooter('bot en fase beta')
message.channel.send(embed);
}

if (message.content === '_pika') {
const embed = new Discord.MessageEmbed()
      .setTitle(':smiling_imp: **PIKA...PIKA** :smiling_imp:')
      .setImage('https://media.discordapp.net/attachments/859137648266182690/860583122848579604/180252523_112322344305380_5857518650018760986_n.png')
      .setColor('#000000')
      .setFooter('bot en fase beta')
message.channel.send(embed);
  }

if (message.content === '_obligame') {
const embed = new Discord.MessageEmbed()
      .setTitle('¡OBLIGAME PRRO!')
      .setImage('https://media.discordapp.net/attachments/859137648077045775/860735050631086100/2Q.png')
      .setColor('#000000')
      .setFooter('bot en fase beta')
message.channel.send(embed);
  }

if (message.content === '_hija') {
    const embed = new Discord.MessageEmbed()
      .setTitle('Titulo embed')
      .setImage('https://images-ext-2.discordapp.net/external/0lgfGmZzCZCkRKJrXtvQUmAv4JYEwwPeQiLdMZN7kgY/%3Fsize%3D2048/https/cdn.discordapp.com/avatars/790057826159558656/d4c2524a9637c3bc666447275fbfe60a.png')
      .setColor('#000000')
      .setFooter('bot en fase beta')
message.channel.send(embed);
}



});

client.login('')
