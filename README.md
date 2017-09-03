# Discord-bot-personal-welcome
Discord bot personal welcome
const commando = require('discord.js-commando');
const bot = new commando.Client();

bot.on('message', message=>{
    if(message.content.startsWith('ping')){
        message.channel.sendMessage(message.author.id);
        //var voiceChannel = message.member.voiceChannel;
        //voiceChannel.join()
          //  .then(connection => {
            //    const dispatcher = connection.playFile('C:/Users/Stefano/Documents/Levante.mp3');
              //  
           // })
            //.catch(err => console.log(err));
            message.channel.sendMessage(message.author)
        
    }
})
bot.on('voiceStateUpdate', (oldMember, newMember) => { //voiceStateUpdate: change channel, mute/unmute
    let newUserChannel = newMember.voiceChannel
    let oldUserChannel = oldMember.voiceChannel


    if(oldUserChannel === undefined && newUserChannel !== undefined) { //Membro entra nel canale
        if(newMember.id==number2){ //se è Stefalber
      var newMemberChannel =  newMember.voiceChannel;
      newMemberChannel.join().then(connection => {
        const dispatcher = connection.playFile('D:/AudioBot/veskim2.ogg');
    })
    .catch(err => console.log(err));
        }else if(newMember.id==number1){ //se è Veskim
            var newMemberChannel =  newMember.voiceChannel;
            newMemberChannel.join().then(connection => {
              const dispatcher = connection.playFile('D:/AudioBot/veskim3.ogg');
          })
        }else{ //se è un tizio a caso
            var newMemberChannel =  newMember.voiceChannel;
            newMemberChannel.join().then(connection => {
              const dispatcher = connection.playFile('D:/AudioBot/veskim1.ogg');
          })
        }
        } else if(newUserChannel === undefined){
        var oldMemberChannel = oldMember.voiceChannel;
        oldMemberChannel.join().then(connection => {
            const dispatcher1 = connection.playFile('D:/AudioBot/veskim2.ogg');
            
        })
        .catch(err => console.log(err));
    

    } else if(newUserChannel.id == number3 //se è già nel server ed entra in General
        var newMemberChannel = newMember.voiceChannel;
        newMemberChannel.join().then(connection => {
            const dispatcher1 = connection.playFile('D:/AudioBot/veskim1.ogg');
            
        })
        .catch(err => console.log(err));
    }
  })


bot.login('MzUyODgwMzQxMzE4NTAwMzY0.DInk9g.2G9T7jRep7xo_AntD_QD39UJ4qA');
