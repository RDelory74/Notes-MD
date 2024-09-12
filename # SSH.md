# SSH 

    ssh-keygen  

~ ❯ ssh-keygen                                                                                                                                                                 09:10:36
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/rodolphe-delory/.ssh/id_ed25519): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/rodolphe-delory/.ssh/id_ed25519
Your public key has been saved in /home/rodolphe-delory/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:g1w8/HAWTzjsPIUuInS/E17VarCrfqxsTWdj4ubPiv4 rodolphe-delory@rodolphe-delory-HP-CNA-102


The key's randomart image is:

        +--[ED25519 256]--+
        |         ..o..   |
        |    . .o  *+o .  |
        |   . . .*+o*..   |
        |    ...o+*B o    |
        |     .ooS=.+     |
        |        +.+ =    |
        |         B = .   |
        |       .o.*.     |
        |       +**Eoo    |
        +----[SHA256]-----+


cat /home/rodolphe-delory/.ssh/id_ed25519.pub                                                                                                                              09:12:17
authorized_keys  id_ed25519       =>id_ed25519.pub 

    ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIK1P6oY6L5IwWYeSPNMFVmmO+2sgQ3vB9JUllbNKoE2K rodolphe-delory@rodolphe-delory-HP-CNA-102

Dans les setting profile sur github selectionez SSH and GPG keys
usage : git remote [-v | --verbose]
   ou : git remote add [-t <branche>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <nom> <url>
   ou : git remote rename [--[no-]progress] <ancien> <nouveau>
   ou : git remote remove <nom>
   ou : git remote set-head <nom> (-a | --auto | -d | --delete | <branche>)
   ou : git remote [-v | --verbose] show [-n] <nom>
   ou : git remote prune [-n | --dry-run] <nom>
   ou : git remote [-v | --verbose] update [-p | --prune] [(<groupe> | <distante>)...]
   ou : git remote set-branches [--add] <nom> <branche>...
   ou : git remote get-url [--push] [--all] <nom>
   ou : git remote set-url [--push] <nom> <nouvelle-URL> [<ancienne-URL>]
   ou : git remote set-url --add <nom> <nouvelle-URL>
   ou : git remote set-url --delete <nom> <url>
depuis github cloner le projet avec le lien SSH puis entrez la commande suivante sur le main du projet:

    main* ❯ git remote set-url origin git@github.com:rmMoumenCampusNum/REZ_GAMES.git


php artisan make:controller NomDuController --resource

namespace App\Http\Controllers;

use App\Models\Item; // Assurez-vous d'importer le modèle Item
use Illuminate\Http\Request;

class ItemController extends Controller
{
    /**
     * Affiche une liste des ressources.
     */
    public function index()
    {
        $items = Item::all(); // Récupère tous les items
        return response()->json($items);
    }

    /**
     * Affiche le formulaire pour créer une nouvelle ressource.
     */
    public function create()
    {
        // Retourne une vue si nécessaire
    }

    /**
     * Stocke une nouvelle ressource dans le stockage.
     */
    public function store(Request $request)
    {
        $item = Item::create($request->all()); // Crée un nouvel item
        return response()->json($item, 201);
    }

    /**
     * Affiche la ressource spécifiée.
     */
    public function show(string $id)
    {
        $item = Item::findOrFail($id); // Trouve l'item par ID
        return response()->json($item);
    }

    /**
     * Affiche le formulaire pour modifier la ressource spécifiée.
     */
    public function edit(string $id)
    {
        // Retourne une vue si nécessaire
    }

    /**
     * Met à jour la ressource spécifiée dans le stockage.
     */
    public function update(Request $request, string $id)
    {
        $item = Item::findOrFail($id); // Trouve l'item
        $item->update($request->all()); // Met à jour l'item
        return response()->json($item);
    }

    /**
     * Supprime la ressource spécifiée du stockage.
     */
    public function destroy(string $id)
    {
        $item = Item::findOrFail($id); // Trouve l'item
        $item->delete(); // Supprime l'item
        
        https://www.youtube.com/watch?v=olf35zb2YS0


        https://www.youtube.com/watch?v=olf35zb2YS0


Generating public/private rsa key pair.
Enter file in which to save the key (/home/rodolphe-delory/.ssh/id_rsa):                                                
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/rodolphe-delory/.ssh/id_rsa
Your public key has been saved in /home/rodolphe-delory/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:vGhjZ2VQUfDdTZvppVDLuhsMgHH4HnmUE3Su3suEJkI rodolphe-delory@rodolphe-delory-HP-CNA-102
The key's randomart image is:
+---[RSA 3072]----+
|      ....**o . .|
|      .+ .++ + +=|
|      ..oo .+ +++|
|       .+o.. o...|
|      E.So= . .. |
|     . ..= = .   |
|      * = + *    |
|     o = o o +   |
|            +    |
+----[SHA256]-----+
