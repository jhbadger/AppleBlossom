# Apple Blossom Village

*A turn-based farming game of seasons, crops and neighbours, in Python and Tk.*

Your grandmother Lily has left you her farm at the edge of Apple Blossom
Village. It has stood empty for years: the fields are full of weeds, stones
and fallen branches, but her tools are still good and the shipping bin by the
door still works. Clear the land, grow crops, and get to know the twelve
people of the village. Six of them might come to love you.

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
| Fishing rod | ask Theo about FISHING; face water and cast |
| Magic wand | casts petrify straight ahead (see below) |

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

## The magic wand

Among Grandmother's tools is a **magic wand**. (Someday it will be the reward
for a quest; for now you start with it.) Hold it and use it (Space, E, the Use
button, or tap yourself) and choose a spell. Then pick a direction: an arrow
key, a tap on that side of you, or the d-pad. Anyone the spell would hit is
ringed in gold while you aim. Space zaps the way you're facing, and Esc lowers
the wand. With the wand in hand you can also just tap a villager who's in a
straight line from you, which casts the spell you last chose. The spell flies
up to eight squares until it hits someone or something solid.

- **Petrify** turns whoever it hits into a golden statue. A statue can't move
  or talk. Walk into one and you polish it, rub its nose for luck, or knock on
  it to hear it ring. Petrify a statue again and it turns back into the
  villager, who has something to say about it.
- **Genderswap**, after Homeroom's Boy/Girl Gun, turns whoever it hits into the
  other sex. Their sprite and portrait change: face, build and hairstyle,
  beards and moustaches gone, and Granny Rose becomes Grandpa Rose. Each game
  some villagers like it and some hate it, and each says so in their own
  voice. They greet you accordingly and will tell you about the CHANGE. Liking
  it earns you friendship (once); hating it costs you. Cast it again to change
  them back, which pleases the ones who hated it and disappoints the ones who
  liked it. You can swap a statue too, but it doesn't mind.

## The village

| Place | Who | What's there |
| --- | --- | --- |
| Pike's General Store | Mabel Pike | seeds for the season, gifts, the Blossom Bouquet |
| Blossom Inn | Bernard and Wren Calloway | meals that restore energy; Wren plays fiddle Friday and Saturday nights |
| The Clinic | Dr. Felix Thorne | energy tonics and a daily checkup |
| Brandt Smithy | Otto Brandt and Rowan Hale | sprinklers, the copper watering can, fine gifts, the Blossom Pendant |
| Larkin Carpentry | Ivy Larkin (and her brother Pip) | wood, and the cabin extension |
| The dock | Theo Fairweather | fishing rods and lures, 10 till 3 |
| The Library | Juniper Marsh | books, and Pip's schoolroom |
| Mayor's House | Mayor Edmund Pell | festivals, history |
| Rose's Cottage | Granny Rose Applewood | your grandmother's cousin, and pie |

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
ABOUT... asks what they think of the others. Words in CAPITALS are worth
asking about. Each villager has their own topics, opinions, secrets and
sense of humour.

**Friendship** is counted in hearts, up to ten:

- Talk to someone every day.
- Give gifts, up to two a week each. Everyone has things they love, like,
  dislike and hate. A gift on their birthday counts five times over.
- At certain heart levels a friend shares a **moment** with you: a short scene,
  often with a choice to make. Rowan's wooden fox, Felix's dying lavender,
  Mabel's thieving cat, Pip's treasure hunt, and more.

**Romance.** Rowan, Felix, Theo, Juniper, Wren and Ivy can become more than
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
