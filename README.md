# Apple Blossom Village

*A turn-based farming game of seasons, crops and neighbours, in Python and Tk.*

Your grandmother Lily has left you her farm at the edge of Apple Blossom
Village. It has stood empty for years: the fields are full of weeds, stones
and fallen branches, but her tools are still good and the shipping bin by the
door still works. Clear the land, grow crops, and get to know the fourteen
people of the village. Eight of them might come to love you.

It's one executable script on the tilerpgs engine: a map of squares, people
you talk to by keyword, shops, and tiles, portraits and music all drawn in
code. There are no image or sound files.

## Running it

It needs only Python 3 with Tk, and nothing else to install.

```bash
./appleblossomvillage
```

If Python reports `No module named '_tkinter'`, install your Python's Tk
package (`brew install python-tk` with Homebrew Python, or
`sudo apt install python3-tk` on Debian and Ubuntu).

On macOS, `./appleblossomvillage --build-app [DIR]` builds an
`appleblossomvillage.app` with its own icon (an apple blossom), and
`--icon-png SIZE [OUT.png]` writes just the icon. `--selftest` builds the
valley, every room, portrait and tune and checks that the villagers'
schedules, gifts and scenes all fit together.

## Your farmer

A new game starts by asking who you are: your name, your farm's name, how
people should refer to you (they, she or he), and how you look. You pick your
build, hairstyle, hair colour, skin, eyes, shirt and trousers. The dialog
shows both the small sprite you walk around as and the large portrait.

## Time

Each step takes a minute and each swing of a tool three. Days run from six in
the morning until two at night. If you're still up at two you collapse, and Dr.
Thorne carries you home and sends a bill. Walk into your bed to sleep. There
are four seasons of 28 days, and the grass, trees, roofs and music change with
each one. Nights get dark: lamps and your own lantern light the way.

## The farm

Hold a tool and use it on the square in front of you, which is outlined when
the tool would do something there.

| Tool | What it does |
| --- | --- |
| Hoe | tills grass on your farm into soil, and clears dead plants |
| Watering can | waters soil; fill it at the well, the pond, the river or the lake |
| Seeds | go into tilled soil, in their season |
| Axe, pickaxe, scythe | clear branches and stumps, stones, and weeds (walking into debris uses the right one) |
| Axe, on a tree | three swings fell it, for 8 wood and a stump to clear (6 more); it grows back after a season |
| Fishing rod | ask Theo about FISHING; face water and cast |
| Magic wand | casts a spell straight ahead (see below) |
| Leash | from Mabel's: leads a chickenfied or cowified villager, and lets her go again (see below) |
| Milk pail | from Mabel's: milks a cow in your barn, once a day each |

Watered crops grow a day each night, and rain waters them for you. When a crop
is ripe, use anything on it to pick it. Some crops (strawberries, tomatoes,
corn, blueberries, cranberries, eggplant) keep producing after picking. A crop
dies if its season ends before you pick it. There are 14 crops: turnip, potato,
strawberry, cauliflower and pea in spring; tomato, corn, melon, blueberry and
sunflower in summer; and pumpkin, cranberry, yam, eggplant and corn in fall.

Put anything sellable in the **shipping bin** and you're paid overnight.
Grandmother's apple trees fruit in the fall. Wild things to forage turn up in
the woods, the meadows and on the beach every morning. Otto's **sprinklers**
water the four squares around them each morning.

### Chickens

Ivy will build you a **chicken coop** beside your cabin for 1,500g and 80
wood. Once it's up, Mabel sells **hens** at 800g each, up to eight. Each hen
arrives with a random name (Clucky, Henrietta, Lady Cluckington, Omelette,
and others) and a colour (white, brown, black or speckled). Hens potter about
the coop while you're there.

- **Eggs:** every hen lays an egg each night, somewhere on the coop floor.
  Walk over an egg to pick it up. Eggs sell for 50g, give 15 energy eaten,
  and Bernard and Granny Rose like them as gifts.
- **Your hens:** walk into a hen to pet her (once a day) or to give her a new
  name. Type the name in the bar under the map and press Return; Esc keeps
  the old one. The Friends list (F) shows your hens and which you've petted
  today.

### Cows

Ivy will also build you a **barn** up by your fields for 4,000g, 150 wood
and 50 stone. Once it's up, Mabel sells **cows** at 1,500g each, up to six,
and a **milk pail** (300g, and you keep it). Each cow comes with a name
(Buttercup, Clover, Bessie, Custard, and others) and a coat (spotted, brown,
black or ginger), and wanders the barn while you're there.

- **Milk:** with the pail in hand, use it on a cow, or walk into her and
  choose Milk, once a day each. Milk sells for 125g and gives 25 energy.
- **Your cows:** walk into a cow to pet her (once a day), rename her or
  milk her. The Friends list shows your cows.

## The magic wand

Among Grandmother's tools is a **magic wand**. (Someday it will be the reward
for a quest; for now you start with it.) Hold it and use it (Space, E, the Use
button, or tap yourself) and choose a spell. Then pick a direction: an arrow
key, a tap on that side of you, or the d-pad. Anyone the spell would hit is
ringed in gold while you aim. Space zaps the way you're facing, and Esc lowers
the wand. With the wand in hand you can also just tap a villager who's in a
straight line from you, choose a spell, and it flies at them. The spell flies
up to eight squares until it hits someone or something solid.

- **Petrify** turns whoever it hits into a golden statue. A statue can't move
  or talk. Walk into one and you polish it, rub its nose for luck, or knock on
  it to hear it ring; walk into it again straight away and you squeeze past
  it. Petrify a statue again and it turns back into the
  villager, who has something to say about it.
- **Genderswap**, after Homeroom's Boy/Girl Gun, turns whoever it hits into the
  other sex. Their sprite and portrait change: face, build and hairstyle,
  beards and moustaches gone, and Granny Rose becomes Grandpa Rose. Each game
  some villagers like it and some hate it, and each says so in their own
  voice. They greet you accordingly and will tell you about the CHANGE. Liking
  it earns you friendship (once); hating it costs you. Cast it again to change
  them back, which pleases the ones who hated it and disappoints the ones who
  liked it. You can swap a statue too, but it doesn't mind.
- **Chickenfy** turns whoever it hits into a hen just like the ones Mabel
  sells, in a colour that suits their hair. The hen goes on with the
  villager's day: Theo the hen still minds the tackle stand, and Wren the hen
  still turns up at the inn. A hen can't talk. Walk into one and she clucks
  happily or clucks angrily, then scuttles past you, depending on whether
  this villager likes being a
  chicken (dealt each game, separately from genderswap). As with genderswap,
  liking it earns you friendship (once) and hating it costs you. Cast it again
  to turn them back, and they'll tell you all about it. Genderswap bounces off
  a chicken; petrify makes a golden hen.

  Mabel sells a **leash** (250g, and you keep it). Use it on a chickenfied
  villager and she follows at your heels wherever you go, instead of
  keeping to her day. Use any tool on her, the leash included, and you let
  her go. Lead her into your coop and she becomes one of your hens: she
  lays an egg each night and can be petted (a villager who likes being a
  chicken takes that as a liked gift), though she keeps her own name. Other
  spells fizzle in the straw; chickenfy her there and she's herself again,
  and off she goes back to her usual routine. The leash holds one hen at a
  time, and a villager-hen takes up a place in the coop like any other.
- **Cowify** turns whoever it hits into a cow like the ones Mabel sells, in
  a coat that suits their hair, and like a chickenfied villager she goes
  on with her day. Walk into her and she moos happily or angrily, depending
  on whether this villager likes being a cow (dealt each game), with
  friendship to match. Put the **leash** on her and she plods after you;
  lead her into your **barn** and she's one of your cows: pet her (a
  villager who likes being a cow takes it as a liked gift) and milk her
  once a day. She won't fit through the coop door. Cowify her again, in the
  barn or out, and she's herself, off back to her routine. Other spells
  bounce off a cow's hide (petrify makes a golden cow), cowify won't take
  on a statue, hen, maid, tree or outhouse, and Pip is too young for it.
- **Maidify** turns whoever it hits into a maid: a young woman in a black
  dress, a white apron and a frilled cap, whoever they were before. She
  moves into your cabin and stops keeping shop. Ask her about her **CHORE**
  and she'll do it every morning before you wake:

  | Chore | What she does |
  | --- | --- |
  | Pick ripe crops | picks everything ripe and puts it in your bag |
  | Clear the fields | clears up to a dozen weeds, stones and branches, and bags what they drop |
  | Water the crops | waters every crop (not needed when it rains) |
  | Collect the eggs | gathers the coop's eggs and pets every hen |
  | Milk the cows | milks every cow in your barn that hasn't been milked |
  | Cook breakfast | leaves you pancakes, bread, honey cake or stew |
  | Just rest | nothing at all |

  You can also **KISS** your maid, twice a day. Each kiss counts as a gift
  she likes, on top of the usual two gifts a week. Maids who'll be outdoors
  spend early mornings in the farmyard. As with
  the other spells, each game some villagers love being a maid and some hate
  it, and it costs or earns you friendship the same way. Either way, a maid
  does exactly what she's told: she just hums or grumbles while she does it.
  Cast it again to set her free. Genderswap and chickenfy glance off a
  maid's apron, maidify bounces off a hen, and Pip's too young for it. The
  Friends list shows each maid's chore.
- **Treeify** turns whoever it hits into a young tree, rooted to the spot,
  with their face peering out of the trunk and a hint of their hair colour
  in the leaves. The tree changes with the seasons: blossom in spring, fruit
  the colour of their shirt in summer, red and gold in fall, snow in winter.
  It stays put, day and night, until you change it back. Walk into it and it
  rustles happily or creaks crossly, depending on whether this villager
  likes being a tree (dealt each game); walk into it again to push through
  the branches. **Water** a tree once a day: one that likes it takes it as a
  gift it likes, one that doesn't shakes the water off at you. You *can*
  take the axe to one: it screams at every swing, and on the third it falls,
  you get the wood, and the villager tumbles out of the trunk, whole but
  shaking and covered in sawdust. That costs a great deal of friendship,
  liked being a tree or not. (Nobody can bring themselves to chop Pip.)
  Friendship goes up or down as with the
  other spells. Cast it again to uproot them and hear about it. Other spells
  sink into the bark without effect, and treeify won't take on a statue, a
  hen or a maid.
- **Looify** turns whoever it hits into an outhouse: a little plank privy
  with a moon on the door, painted the colour of their shirt. It works only
  out of doors, and only where there's clear ground in front for the door to
  open; anywhere else it fizzles. The outhouse stays put until you change it
  back. Walk into it from the front and you go inside, where there's a bench
  with two holes and an old almanac. Walk into a hole and you do your
  business, sometimes to a comment from the walls. Walk into the side and
  you just knock. Villagers passing near an outhouse now and then pop in for
  a few minutes and come out again; if you're inside, they rattle the door
  and hurry off, and if they're inside, you'll hear "Occupied!" As ever,
  some villagers like being an outhouse and some don't, with friendship to
  match. Cast it again to turn them back (anyone inside tumbles out). Other
  spells splinter against the door, looify won't take on a statue, hen,
  maid or tree, and Pip laughs too hard for it to land.

## The village

| Place | Who | What's there |
| --- | --- | --- |
| Pike's General Store | Mabel Pike | seeds for the season, hens, cows, a milk pail, a leash, gifts, the Blossom Bouquet |
| Blossom Inn | Bernard and Wren Calloway | meals that restore energy; Wren plays fiddle Friday and Saturday nights |
| The Clinic | Dr. Felix Thorne | energy tonics and a daily checkup |
| Brandt Smithy | Otto Brandt and Rowan Hale | sprinklers, the copper watering can, fine gifts, the Blossom Pendant |
| Larkin Carpentry | Ivy Larkin (and her brother Pip) | wood, the chicken coop, the barn, and the cabin extension |
| The dock | Theo Fairweather | fishing rods and lures, 10 till 3 |
| The Library | Juniper Marsh | books, and Pip's schoolroom |
| Mayor's House | Mayor Edmund Pell | festivals, history |
| Rose's Cottage | Granny Rose Applewood | your grandmother's cousin, and pie |
| Amy's Cottage | Amy Hartwell | the beekeeper, who sets the Gazette crossword |
| Rusty's Studio | Rusty Quinn | the seamstress and costume-maker, who puts on the play at the inn |

Everyone keeps a daily schedule. They open their shops, take lunch by the
fountain, fish, read on benches, visit each other, gather at the inn in the
evening and go home to bed. Their routine changes on their day off and on
rainy days. You'll see them walk from place to place.

The **notice board** in the square posts requests (bring someone what they
need for a reward), and your **mailbox** gets letters: birthday reminders,
festival notices and news.

## People

Walk into someone to talk. Their **portrait** appears beside what they say,
and it smiles, blushes, frowns or looks surprised as they talk. Choose a word
from the menu or type one: everyone knows CHAT, GIFT, NAME, JOB and NEWS, and
ABOUT... asks what they think of the others, and PAST asks them to step aside
so you can squeeze by, if they're standing in a doorway. Words in CAPITALS are worth
asking about. Each villager has their own topics, opinions, secrets and
sense of humour.

The village notices what your wand gets up to. When you CHAT, people
sometimes bring up somebody you've changed: the golden statue of Otto, the
hen that used to be Theo, Juniper keeping house at your farm, the tree
that's Wren, the outhouse that's Bernard. They wonder whether that person
likes their new life, and drop a hint they've picked up (singing from your
cabin, a branch that shook at them, a door rattling by itself) that tells
you whether they do. Family use their own names: Wren calls Bernard "Dad."

**Friendship** is counted in hearts, up to ten:

- Talk to someone every day.
- Give gifts, up to two a week each. Everyone has things they love, like,
  dislike and hate. A gift on their birthday counts five times over.
- At certain heart levels a friend shares a **moment** with you: a short scene,
  often with a choice to make. Rowan's wooden fox, Felix's dying lavender,
  Mabel's thieving cat, Pip's treasure hunt, and more.

**Romance.** Rowan, Felix, Theo, Juniper, Wren, Ivy, Amy and Rusty can become more than
friends, whoever your farmer is. Each has four heart scenes leading up to a
confession at eight hearts.

1. Give a **Blossom Bouquet** (Mabel's store) to someone at 8 hearts to go
   steady. Sweethearts can reach 10 hearts and can be asked on a **DATE** in
   the evenings.
2. Have Ivy build a **cabin extension** so there's room for two.
3. Give a **Blossom Pendant** (Otto's smithy) to your sweetheart at 10 hearts
   to propose. The wedding is three days later in the square.
4. Your spouse moves into your cabin, still goes to work, and some mornings
   waters the crops or leaves you breakfast.

## Festivals

| Day | Festival | What to do |
| --- | --- | --- |
| Spring 13 | Apple Blossom Festival, in the square | ask someone with 4+ hearts to DANCE |
| Summer 16 | Lakeside Picnic, on the beach | SHARE food with Bernard for everyone |
| Fall 16 | Harvest Fair, in the square | ENTER your best crop with the Mayor |
| Winter 24 | Long Night Feast, in the square | give a GIFT to your secret friend |

## Keys

| Key | Action |
| --- | --- |
| Arrows / WASD | move; walk into people, doors, beds, the bin and the mailbox |
| Space / E | use what you're holding on the square ahead |
| Q / Tab, 1-9 | hold the next tool, or a particular one |
| I | your bag: eat, hold, look |
| Z | wait (or sleep, at home) |
| F | friends and hearts |
| J | diary: calendar, birthdays, festivals, requests, letters |
| M | map of the valley |
| ? | help |
| V / B | sound effects / music |
| + / - | zoom |
| Esc | menu |

**Touch and mouse:** tap a square to walk there, tap next to you to step or
use your tool there, tap yourself to use your tool ahead. Menus are tapped.
**Gamepad** (Linux, Steam Deck): d-pad moves, A uses your tool, B backs out,
X next tool, Y bag, LB wait, RB friends, View map, Start menu.

**Screen size:** the whole window scales to fit, on a desktop or a phone
(Pydroid 3 on Android): text, panel, buttons, map tiles and portraits. Held
upright, a phone puts the side panel under the map and the buttons in rows.
Zoom in and out from the menu, and make the text bigger or smaller.

## Files

- `appleblossomvillage`: the game
- `~/.appleblossomvillage.json`: the saved game (written when you change
  place, sleep and quit)
- `~/.cache/appleblossomvillage/`: cached music

## Licence

MIT; see [LICENSE](LICENSE).
