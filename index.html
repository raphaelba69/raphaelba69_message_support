import React, { useState, useEffect } from 'react';
import { Search, Copy, Trash2, RotateCcw, Plus, Settings, BarChart3, Clock, Download, Edit, Save, X, AlertTriangle } from 'lucide-react';

const InterfaceSAV = () => {
  // États pour les critères de recherche
  const [famillesProduits, setFamillesProduits] = useState([]);
  const [typesPannes, setTypesPannes] = useState([]);
  const [sousPannes, setSousPannes] = useState([]);
  const [articles, setArticles] = useState([]);
  const [messagesReponses, setMessagesReponses] = useState([]);
  
  // États pour la recherche
  const [selectedFamille, setSelectedFamille] = useState('');
  const [selectedPanne, setSelectedPanne] = useState('');
  const [selectedSousPanne, setSelectedSousPanne] = useState('');
  const [selectedArticle, setSelectedArticle] = useState('');
  const [messageResultat, setMessageResultat] = useState('');
  
  // États pour l'interface
  const [activeTab, setActiveTab] = useState('recherche');
  const [showAdmin, setShowAdmin] = useState(false);
  const [copySuccess, setCopySuccess] = useState(false);
  const [searchHistory, setSearchHistory] = useState([]);
  const [stats, setStats] = useState({ searchesToday: 0, totalSearches: 0, popularMessages: [] });

  // États pour les modales d'administration
  const [modals, setModals] = useState({
    famille: false,
    panne: false,
    sousPanne: false,
    article: false,
    message: false,
    delete: false
  });
  
  // États pour les formulaires
  const [formData, setFormData] = useState({});
  const [editingItem, setEditingItem] = useState(null);
  const [deleteTarget, setDeleteTarget] = useState(null);

  // Données de base de connaissances (simulation)
  useEffect(() => {
    // Initialisation des données
    const initData = {
      familles: [
        { id: 1, nom: 'Canapé' },
        { id: 2, nom: 'Lit' },
        { id: 3, nom: 'Meuble métal' },
        { id: 4, nom: 'Table' },
        { id: 5, nom: 'Chaise' }
      ],
      pannes: [
        { id: 1, nom: 'Pièce manquante', familleIds: [1, 2, 3, 4, 5] },
        { id: 2, nom: 'Bruit', familleIds: [1, 2, 3] },
        { id: 3, nom: 'Usure', familleIds: [1, 2, 4, 5] },
        { id: 4, nom: 'Défaut assemblage', familleIds: [1, 2, 3, 4, 5] },
        { id: 5, nom: 'Rayure/Dommage', familleIds: [1, 2, 3, 4, 5] }
      ],
      sousPannes: [
        { id: 1, nom: 'Vis manquante', panneId: 1 },
        { id: 2, nom: 'Boulon manquant', panneId: 1 },
        { id: 3, nom: 'Grincement', panneId: 2 },
        { id: 4, nom: 'Claquement', panneId: 2 },
        { id: 5, nom: 'Rayure surface', panneId: 5 },
        { id: 6, nom: 'Coin cassé', panneId: 5 }
      ],
      articles: [
        { id: 1, reference: 'CAP-001', nom: 'Canapé 3 places Lincoln', familleId: 1 },
        { id: 2, reference: 'LIT-002', nom: 'Lit 140x190 Emma', familleId: 2 },
        { id: 3, reference: 'MET-003', nom: 'Étagère métal industriel', familleId: 3 }
      ],
      messages: [
        {
          id: 1,
          familleId: 1,
          panneId: 1,
          sousPanneId: 1,
          articleId: null,
          contenu: `Bonjour,

Nous sommes désolés pour ce désagrément concernant votre canapé. 

🔧 **Solution immédiate :**
Nous vous envoyons par courrier les vis manquantes dans les 48h.

📦 **Contenu du colis :**
- 4 vis M6x20mm
- 2 rondelles
- Notice de montage

💡 **En attendant :** Vous pouvez utiliser temporairement des vis similaires disponibles en magasin de bricolage.

Cordialement,
L'équipe SAV`
        },
        {
          id: 2,
          familleId: 2,
          panneId: 2,
          sousPanneId: 3,
          articleId: null,
          contenu: `Bonjour,

Merci de nous avoir contactés concernant le grincement de votre lit.

🔍 **Diagnostic :**
Ce bruit provient généralement des fixations qui se sont desserrées avec le temps.

🛠️ **Solution :**
1. Vérifiez et resserrez toutes les vis du sommier
2. Appliquez un peu de graisse sur les points de contact
3. Vérifiez que le lit est bien stable au sol

📞 Si le problème persiste, n'hésitez pas à nous recontacter.

Cordialement,
L'équipe SAV`
        }
      ]
    };

    setFamillesProduits(initData.familles);
    setTypesPannes(initData.pannes);
    setSousPannes(initData.sousPannes);
    setArticles(initData.articles);
    setMessagesReponses(initData.messages);
  }, []);

  // Fonction pour générer un nouvel ID
  const generateId = (array) => {
    return Math.max(...array.map(item => item.id), 0) + 1;
  };

  // Fonctions pour ouvrir les modales
  const openModal = (type, item = null) => {
    setEditingItem(item);
    setFormData(item || {});
    setModals(prev => ({ ...prev, [type]: true }));
  };

  const closeModal = (type) => {
    setModals(prev => ({ ...prev, [type]: false }));
    setEditingItem(null);
    setFormData({});
  };

  const openDeleteModal = (type, item) => {
    setDeleteTarget({ type, item });
    setModals(prev => ({ ...prev, delete: true }));
  };

  // Fonctions de gestion des données
  const handleSaveFamille = () => {
    if (!formData.nom?.trim()) return;
    
    if (editingItem) {
      setFamillesProduits(prev => prev.map(f => 
        f.id === editingItem.id ? { ...f, nom: formData.nom } : f
      ));
    } else {
      const newFamille = {
        id: generateId(famillesProduits),
        nom: formData.nom
      };
      setFamillesProduits(prev => [...prev, newFamille]);
    }
    closeModal('famille');
  };

  const handleSavePanne = () => {
    if (!formData.nom?.trim() || !formData.familleIds?.length) return;
    
    if (editingItem) {
      setTypesPannes(prev => prev.map(p => 
        p.id === editingItem.id ? { ...p, nom: formData.nom, familleIds: formData.familleIds } : p
      ));
    } else {
      const newPanne = {
        id: generateId(typesPannes),
        nom: formData.nom,
        familleIds: formData.familleIds
      };
      setTypesPannes(prev => [...prev, newPanne]);
    }
    closeModal('panne');
  };

  const handleSaveSousPanne = () => {
    if (!formData.nom?.trim() || !formData.panneId) return;
    
    if (editingItem) {
      setSousPannes(prev => prev.map(sp => 
        sp.id === editingItem.id ? { ...sp, nom: formData.nom, panneId: formData.panneId } : sp
      ));
    } else {
      const newSousPanne = {
        id: generateId(sousPannes),
        nom: formData.nom,
        panneId: parseInt(formData.panneId)
      };
      setSousPannes(prev => [...prev, newSousPanne]);
    }
    closeModal('sousPanne');
  };

  const handleSaveArticle = () => {
    if (!formData.reference?.trim() || !formData.nom?.trim() || !formData.familleId) return;
    
    if (editingItem) {
      setArticles(prev => prev.map(a => 
        a.id === editingItem.id ? { ...a, reference: formData.reference, nom: formData.nom, familleId: formData.familleId } : a
      ));
    } else {
      const newArticle = {
        id: generateId(articles),
        reference: formData.reference,
        nom: formData.nom,
        familleId: parseInt(formData.familleId)
      };
      setArticles(prev => [...prev, newArticle]);
    }
    closeModal('article');
  };

  const handleSaveMessage = () => {
    if (!formData.contenu?.trim()) return;
    
    if (editingItem) {
      setMessagesReponses(prev => prev.map(m => 
        m.id === editingItem.id ? { 
          ...m, 
          familleId: formData.familleId ? parseInt(formData.familleId) : null,
          panneId: formData.panneId ? parseInt(formData.panneId) : null,
          sousPanneId: formData.sousPanneId ? parseInt(formData.sousPanneId) : null,
          articleId: formData.articleId ? parseInt(formData.articleId) : null,
          contenu: formData.contenu 
        } : m
      ));
    } else {
      const newMessage = {
        id: generateId(messagesReponses),
        familleId: formData.familleId ? parseInt(formData.familleId) : null,
        panneId: formData.panneId ? parseInt(formData.panneId) : null,
        sousPanneId: formData.sousPanneId ? parseInt(formData.sousPanneId) : null,
        articleId: formData.articleId ? parseInt(formData.articleId) : null,
        contenu: formData.contenu
      };
      setMessagesReponses(prev => [...prev, newMessage]);
    }
    closeModal('message');
  };

  const handleDelete = () => {
    const { type, item } = deleteTarget;
    
    switch(type) {
      case 'famille':
        setFamillesProduits(prev => prev.filter(f => f.id !== item.id));
        break;
      case 'panne':
        setTypesPannes(prev => prev.filter(p => p.id !== item.id));
        setSousPannes(prev => prev.filter(sp => sp.panneId !== item.id));
        break;
      case 'sousPanne':
        setSousPannes(prev => prev.filter(sp => sp.id !== item.id));
        break;
      case 'article':
        setArticles(prev => prev.filter(a => a.id !== item.id));
        break;
      case 'message':
        setMessagesReponses(prev => prev.filter(m => m.id !== item.id));
        break;
    }
    
    setModals(prev => ({ ...prev, delete: false }));
    setDeleteTarget(null);
  };

  // Fonction de recherche
  const handleSearch = () => {
    let messageFound = null;

    // Recherche par référence article d'abord
    if (selectedArticle) {
      const article = articles.find(a => a.reference === selectedArticle || a.id.toString() === selectedArticle);
      if (article) {
        messageFound = messagesReponses.find(m => m.articleId === article.id);
      }
    }

    // Recherche combinée si pas trouvé par article
    if (!messageFound) {
      messageFound = messagesReponses.find(m => {
        const matchFamille = !selectedFamille || m.familleId?.toString() === selectedFamille;
        const matchPanne = !selectedPanne || m.panneId?.toString() === selectedPanne;
        const matchSousPanne = !selectedSousPanne || m.sousPanneId?.toString() === selectedSousPanne;
        return matchFamille && matchPanne && matchSousPanne;
      });
    }

    if (messageFound) {
      setMessageResultat(messageFound.contenu);
      
      // Ajouter à l'historique
      const newSearch = {
        id: Date.now(),
        timestamp: new Date().toLocaleString(),
        criteres: {
          famille: selectedFamille ? famillesProduits.find(f => f.id.toString() === selectedFamille)?.nom : '',
          panne: selectedPanne ? typesPannes.find(p => p.id.toString() === selectedPanne)?.nom : '',
          sousPanne: selectedSousPanne ? sousPannes.find(s => s.id.toString() === selectedSousPanne)?.nom : '',
          article: selectedArticle
        },
        message: messageFound.contenu.substring(0, 100) + '...'
      };
      setSearchHistory(prev => [newSearch, ...prev.slice(0, 9)]);
      
      // Mettre à jour les stats
      setStats(prev => ({
        ...prev,
        searchesToday: prev.searchesToday + 1,
        totalSearches: prev.totalSearches + 1
      }));
    } else {
      setMessageResultat('Aucun message type trouvé pour ces critères. Veuillez contacter l\'administrateur pour ajouter une réponse.');
    }
  };

  // Fonction pour effacer les critères
  const handleClear = () => {
    setSelectedFamille('');
    setSelectedPanne('');
    setSelectedSousPanne('');
    setSelectedArticle('');
  };

  // Fonction pour nouvelle recherche
  const handleNewSearch = () => {
    handleClear();
    setMessageResultat('');
  };

  // Fonction pour copier le message
  const handleCopy = async () => {
    if (messageResultat) {
      try {
        await navigator.clipboard.writeText(messageResultat);
        setCopySuccess(true);
        setTimeout(() => setCopySuccess(false), 2000);
      } catch (err) {
        console.error('Erreur lors de la copie:', err);
      }
    }
  };

  // Filtrer les sous-pannes selon la panne sélectionnée
  const filteredSousPannes = sousPannes.filter(sp => 
    !selectedPanne || sp.panneId.toString() === selectedPanne
  );

  // Filtrer les pannes selon la famille sélectionnée
  const filteredPannes = typesPannes.filter(p => 
    !selectedFamille || p.familleIds.includes(parseInt(selectedFamille))
  );

  // Composant Modal générique
  const Modal = ({ isOpen, onClose, title, children }) => {
    if (!isOpen) return null;
    
    return (
      <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 p-4">
        <div className="bg-white rounded-lg shadow-xl max-w-2xl w-full max-h-[90vh] overflow-y-auto">
          <div className="flex items-center justify-between p-6 border-b">
            <h3 className="text-lg font-semibold text-gray-800">{title}</h3>
            <button
              onClick={onClose}
              className="text-gray-400 hover:text-gray-600 transition-colors"
            >
              <X className="w-6 h-6" />
            </button>
          </div>
          <div className="p-6">
            {children}
          </div>
        </div>
      </div>
    );
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 p-4">
      <div className="max-w-6xl mx-auto">
        {/* Header */}
        <div className="bg-white rounded-lg shadow-lg p-6 mb-6">
          <div className="flex items-center justify-between">
            <div>
              <h1 className="text-3xl font-bold text-gray-800 mb-2">🛠️ Interface SAV</h1>
              <p className="text-gray-600">Recherche de messages types pour le support client</p>
            </div>
            <div className="flex gap-2">
              <button
                onClick={() => setActiveTab('recherche')}
                className={`px-4 py-2 rounded-lg font-medium transition-colors ${
                  activeTab === 'recherche' 
                    ? 'bg-blue-500 text-white' 
                    : 'bg-gray-100 text-gray-700 hover:bg-gray-200'
                }`}
              >
                <Search className="inline w-4 h-4 mr-2" />
                Recherche
              </button>
              <button
                onClick={() => setActiveTab('historique')}
                className={`px-4 py-2 rounded-lg font-medium transition-colors ${
                  activeTab === 'historique' 
                    ? 'bg-blue-500 text-white' 
                    : 'bg-gray-100 text-gray-700 hover:bg-gray-200'
                }`}
              >
                <Clock className="inline w-4 h-4 mr-2" />
                Historique
              </button>
              <button
                onClick={() => setActiveTab('stats')}
                className={`px-4 py-2 rounded-lg font-medium transition-colors ${
                  activeTab === 'stats' 
                    ? 'bg-blue-500 text-white' 
                    : 'bg-gray-100 text-gray-700 hover:bg-gray-200'
                }`}
              >
                <BarChart3 className="inline w-4 h-4 mr-2" />
                Statistiques
              </button>
              <button
                onClick={() => setShowAdmin(!showAdmin)}
                className="px-4 py-2 rounded-lg font-medium bg-green-100 text-green-700 hover:bg-green-200 transition-colors"
              >
                <Settings className="inline w-4 h-4 mr-2" />
                Admin
              </button>
            </div>
          </div>
        </div>

        {/* Interface de recherche */}
        {activeTab === 'recherche' && (
          <div className="grid grid-cols-1 lg:grid-cols-2 gap-6">
            {/* Zone de critères */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <h2 className="text-xl font-semibold text-gray-800 mb-4">🔍 Critères de recherche</h2>
              
              <div className="space-y-4">
                {/* Famille produit */}
                <div>
                  <label className="block text-sm font-medium text-gray-700 mb-2">
                    Famille produit
                  </label>
                  <select
                    value={selectedFamille}
                    onChange={(e) => setSelectedFamille(e.target.value)}
                    className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                  >
                    <option value="">-- Sélectionnez une famille --</option>
                    {famillesProduits.map(famille => (
                      <option key={famille.id} value={famille.id}>
                        {famille.nom}
                      </option>
                    ))}
                  </select>
                </div>

                {/* Type de panne */}
                <div>
                  <label className="block text-sm font-medium text-gray-700 mb-2">
                    Type de panne
                  </label>
                  <select
                    value={selectedPanne}
                    onChange={(e) => setSelectedPanne(e.target.value)}
                    className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                  >
                    <option value="">-- Sélectionnez un type de panne --</option>
                    {filteredPannes.map(panne => (
                      <option key={panne.id} value={panne.id}>
                        {panne.nom}
                      </option>
                    ))}
                  </select>
                </div>

                {/* Sous-panne */}
                <div>
                  <label className="block text-sm font-medium text-gray-700 mb-2">
                    Sous-panne
                  </label>
                  <select
                    value={selectedSousPanne}
                    onChange={(e) => setSelectedSousPanne(e.target.value)}
                    className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                    disabled={!selectedPanne}
                  >
                    <option value="">-- Sélectionnez une sous-panne --</option>
                    {filteredSousPannes.map(sousPanne => (
                      <option key={sousPanne.id} value={sousPanne.id}>
                        {sousPanne.nom}
                      </option>
                    ))}
                  </select>
                </div>

                {/* Référence article */}
                <div>
                  <label className="block text-sm font-medium text-gray-700 mb-2">
                    Référence article
                  </label>
                  <select
                    value={selectedArticle}
                    onChange={(e) => setSelectedArticle(e.target.value)}
                    className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                  >
                    <option value="">-- Sélectionnez un article --</option>
                    {articles.map(article => (
                      <option key={article.id} value={article.reference}>
                        {article.reference} - {article.nom}
                      </option>
                    ))}
                  </select>
                </div>

                {/* Boutons d'action */}
                <div className="flex flex-wrap gap-2 pt-4">
                  <button
                    onClick={handleSearch}
                    className="flex items-center px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
                  >
                    <Search className="w-4 h-4 mr-2" />
                    Rechercher
                  </button>
                  <button
                    onClick={handleClear}
                    className="flex items-center px-4 py-2 bg-gray-500 text-white rounded-lg hover:bg-gray-600 transition-colors"
                  >
                    <Trash2 className="w-4 h-4 mr-2" />
                    Effacer
                  </button>
                  <button
                    onClick={handleNewSearch}
                    className="flex items-center px-4 py-2 bg-orange-500 text-white rounded-lg hover:bg-orange-600 transition-colors"
                  >
                    <RotateCcw className="w-4 h-4 mr-2" />
                    Nouvelle recherche
                  </button>
                </div>
              </div>
            </div>

            {/* Zone de résultats */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <div className="flex items-center justify-between mb-4">
                <h2 className="text-xl font-semibold text-gray-800">💬 Message type</h2>
                {messageResultat && (
                  <button
                    onClick={handleCopy}
                    className={`flex items-center px-4 py-2 rounded-lg transition-colors ${
                      copySuccess 
                        ? 'bg-green-500 text-white' 
                        : 'bg-blue-500 text-white hover:bg-blue-600'
                    }`}
                  >
                    <Copy className="w-4 h-4 mr-2" />
                    {copySuccess ? 'Copié !' : 'Copier la réponse'}
                  </button>
                )}
              </div>
              
              <div className="min-h-[300px] p-4 bg-gray-50 rounded-lg border-2 border-dashed border-gray-300">
                {messageResultat ? (
                  <div className="whitespace-pre-wrap text-gray-800 leading-relaxed">
                    {messageResultat}
                  </div>
                ) : (
                  <div className="flex items-center justify-center h-full text-gray-500 text-center">
                    <div>
                      <Search className="w-12 h-12 mx-auto mb-4 opacity-50" />
                      <p>Sélectionnez vos critères et cliquez sur "Rechercher"</p>
                      <p className="text-sm mt-2">Le message type s'affichera ici</p>
                    </div>
                  </div>
                )}
              </div>
            </div>
          </div>
        )}

        {/* Historique */}
        {activeTab === 'historique' && (
          <div className="bg-white rounded-lg shadow-lg p-6">
            <h2 className="text-xl font-semibold text-gray-800 mb-4">📋 Historique des recherches</h2>
            {searchHistory.length > 0 ? (
              <div className="space-y-3">
                {searchHistory.map(search => (
                  <div key={search.id} className="p-4 bg-gray-50 rounded-lg border">
                    <div className="flex justify-between items-start mb-2">
                      <div className="text-sm text-gray-600">{search.timestamp}</div>
                    </div>
                    <div className="text-sm space-y-1">
                      {search.criteres.famille && <span className="inline-block bg-blue-100 text-blue-800 px-2 py-1 rounded mr-2">👉 {search.criteres.famille}</span>}
                      {search.criteres.panne && <span className="inline-block bg-red-100 text-red-800 px-2 py-1 rounded mr-2">⚠️ {search.criteres.panne}</span>}
                      {search.criteres.sousPanne && <span className="inline-block bg-yellow-100 text-yellow-800 px-2 py-1 rounded mr-2">🔧 {search.criteres.sousPanne}</span>}
                      {search.criteres.article && <span className="inline-block bg-green-100 text-green-800 px-2 py-1 rounded mr-2">📦 {search.criteres.article}</span>}
                    </div>
                    <div className="text-sm text-gray-600 mt-2">{search.message}</div>
                  </div>
                ))}
              </div>
            ) : (
              <div className="text-center text-gray-500 py-8">
                <Clock className="w-12 h-12 mx-auto mb-4 opacity-50" />
                <p>Aucune recherche effectuée</p>
              </div>
            )}
          </div>
        )}

        {/* Statistiques */}
        {activeTab === 'stats' && (
          <div className="bg-white rounded-lg shadow-lg p-6">
            <h2 className="text-xl font-semibold text-gray-800 mb-4">📊 Statistiques d'utilisation</h2>
            <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
              <div className="bg-blue-50 p-4 rounded-lg">
                <div className="text-2xl font-bold text-blue-600">{stats.searchesToday}</div>
                <div className="text-sm text-blue-800">Recherches aujourd'hui</div>
              </div>
              <div className="bg-green-50 p-4 rounded-lg">
                <div className="text-2xl font-bold text-green-600">{stats.totalSearches}</div>
                <div className="text-sm text-green-800">Total des recherches</div>
              </div>
              <div className="bg-purple-50 p-4 rounded-lg">
                <div className="text-2xl font-bold text-purple-600">{messagesReponses.length}</div>
                <div className="text-sm text-purple-800">Messages disponibles</div>
              </div>
            </div>
          </div>
        )}

        {/* Interface d'administration */}
        {showAdmin && (
          <div className="mt-6 space-y-6">
            {/* Boutons d'ajout */}
            <div className="bg-white rounded-lg shadow-lg p-6 border-l-4 border-green-500">
              <h2 className="text-xl font-semibold text-gray-800 mb-4">⚙️ Administration - Ajouter</h2>
              <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-4">
                <button 
                  onClick={() => openModal('famille')}
                  className="p-4 bg-green-50 rounded-lg border border-green-200 hover:bg-green-100 transition-colors"
                >
                  <Plus className="w-6 h-6 mx-auto mb-2 text-green-600" />
                  <div className="text-sm font-medium text-green-800">Ajouter famille</div>
                </button>
                <button 
                  onClick={() => openModal('panne')}
                  className="p-4 bg-blue-50 rounded-lg border border-blue-200 hover:bg-blue-100 transition-colors"
                >
                  <Plus className="w-6 h-6 mx-auto mb-2 text-blue-600" />
                  <div className="text-sm font-medium text-blue-800">Ajouter panne</div>
                </button>
                <button 
                  onClick={() => openModal('sousPanne')}
                  className="p-4 bg-purple-50 rounded-lg border border-purple-200 hover:bg-purple-100 transition-colors"
                >
                  <Plus className="w-6 h-6 mx-auto mb-2 text-purple-600" />
                  <div className="text-sm font-medium text-purple-800">Ajouter sous-panne</div>
                </button>
                <button 
                  onClick={() => openModal('article')}
                  className="p-4 bg-orange-50 rounded-lg border border-orange-200 hover:bg-orange-100 transition-colors"
                >
                  <Plus className="w-6 h-6 mx-auto mb-2 text-orange-600" />
                  <div className="text-sm font-medium text-orange-800">Ajouter article</div>
                </button>
                <button 
                  onClick={() => openModal('message')}
                  className="p-4 bg-indigo-50 rounded-lg border border-indigo-200 hover:bg-indigo-100 transition-colors"
                >
                  <Plus className="w-6 h-6 mx-auto mb-2 text-indigo-600" />
                  <div className="text-sm font-medium text-indigo-800">Ajouter message</div>
                </button>
              </div>
            </div>

            {/* Gestion des familles */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <h3 className="text-lg font-semibold text-gray-800 mb-4">👥 Gestion des familles</h3>
              <div className="space-y-2">
                {famillesProduits.map(famille => (
                  <div key={famille.id} className="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                    <span className="font-medium">{famille.nom}</span>
                    <div className="flex gap-2">
                      <button
                        onClick={() => openModal('famille', famille)}
                        className="p-2 text-blue-600 hover:bg-blue-100 rounded"
                      >
                        <Edit className="w-4 h-4" />
                      </button>
                      <button
                        onClick={() => openDeleteModal('famille', famille)}
                        className="p-2 text-red-600 hover:bg-red-100 rounded"
                      >
                        <Trash2 className="w-4 h-4" />
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            </div>

            {/* Gestion des pannes */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <h3 className="text-lg font-semibold text-gray-800 mb-4">⚠️ Gestion des pannes</h3>
              <div className="space-y-2">
                {typesPannes.map(panne => (
                  <div key={panne.id} className="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                    <div>
                      <span className="font-medium">{panne.nom}</span>
                      <div className="text-sm text-gray-600">
                        Familles: {panne.familleIds.map(id => 
                          famillesProduits.find(f => f.id === id)?.nom
                        ).join(', ')}
                      </div>
                    </div>
                    <div className="flex gap-2">
                      <button
                        onClick={() => openModal('panne', panne)}
                        className="p-2 text-blue-600 hover:bg-blue-100 rounded"
                      >
                        <Edit className="w-4 h-4" />
                      </button>
                      <button
                        onClick={() => openDeleteModal('panne', panne)}
                        className="p-2 text-red-600 hover:bg-red-100 rounded"
                      >
                        <Trash2 className="w-4 h-4" />
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            </div>

            {/* Gestion des sous-pannes */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <h3 className="text-lg font-semibold text-gray-800 mb-4">🔧 Gestion des sous-pannes</h3>
              <div className="space-y-2">
                {sousPannes.map(sousPanne => (
                  <div key={sousPanne.id} className="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                    <div>
                      <span className="font-medium">{sousPanne.nom}</span>
                      <div className="text-sm text-gray-600">
                        Panne: {typesPannes.find(p => p.id === sousPanne.panneId)?.nom}
                      </div>
                    </div>
                    <div className="flex gap-2">
                      <button
                        onClick={() => openModal('sousPanne', sousPanne)}
                        className="p-2 text-blue-600 hover:bg-blue-100 rounded"
                      >
                        <Edit className="w-4 h-4" />
                      </button>
                      <button
                        onClick={() => openDeleteModal('sousPanne', sousPanne)}
                        className="p-2 text-red-600 hover:bg-red-100 rounded"
                      >
                        <Trash2 className="w-4 h-4" />
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            </div>

            {/* Gestion des articles */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <h3 className="text-lg font-semibold text-gray-800 mb-4">📦 Gestion des articles</h3>
              <div className="space-y-2">
                {articles.map(article => (
                  <div key={article.id} className="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                    <div>
                      <span className="font-medium">{article.reference} - {article.nom}</span>
                      <div className="text-sm text-gray-600">
                        Famille: {famillesProduits.find(f => f.id === article.familleId)?.nom}
                      </div>
                    </div>
                    <div className="flex gap-2">
                      <button
                        onClick={() => openModal('article', article)}
                        className="p-2 text-blue-600 hover:bg-blue-100 rounded"
                      >
                        <Edit className="w-4 h-4" />
                      </button>
                      <button
                        onClick={() => openDeleteModal('article', article)}
                        className="p-2 text-red-600 hover:bg-red-100 rounded"
                      >
                        <Trash2 className="w-4 h-4" />
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            </div>

            {/* Gestion des messages */}
            <div className="bg-white rounded-lg shadow-lg p-6">
              <h3 className="text-lg font-semibold text-gray-800 mb-4">💬 Gestion des messages</h3>
              <div className="space-y-2">
                {messagesReponses.map(message => (
                  <div key={message.id} className="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                    <div className="flex-1">
                      <div className="text-sm space-y-1 mb-2">
                        {message.familleId && <span className="inline-block bg-blue-100 text-blue-800 px-2 py-1 rounded mr-2">👉 {famillesProduits.find(f => f.id === message.familleId)?.nom}</span>}
                        {message.panneId && <span className="inline-block bg-red-100 text-red-800 px-2 py-1 rounded mr-2">⚠️ {typesPannes.find(p => p.id === message.panneId)?.nom}</span>}
                        {message.sousPanneId && <span className="inline-block bg-yellow-100 text-yellow-800 px-2 py-1 rounded mr-2">🔧 {sousPannes.find(s => s.id === message.sousPanneId)?.nom}</span>}
                        {message.articleId && <span className="inline-block bg-green-100 text-green-800 px-2 py-1 rounded mr-2">📦 {articles.find(a => a.id === message.articleId)?.reference}</span>}
                      </div>
                      <div className="text-sm text-gray-600">
                        {message.contenu.substring(0, 100)}...
                      </div>
                    </div>
                    <div className="flex gap-2 ml-4">
                      <button
                        onClick={() => openModal('message', message)}
                        className="p-2 text-blue-600 hover:bg-blue-100 rounded"
                      >
                        <Edit className="w-4 h-4" />
                      </button>
                      <button
                        onClick={() => openDeleteModal('message', message)}
                        className="p-2 text-red-600 hover:bg-red-100 rounded"
                      >
                        <Trash2 className="w-4 h-4" />
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            </div>
          </div>
        )}

        {/* Modales */}
        
        {/* Modal Famille */}
        <Modal 
          isOpen={modals.famille} 
          onClose={() => closeModal('famille')}
          title={editingItem ? 'Modifier la famille' : 'Ajouter une famille'}
        >
          <div className="space-y-4">
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Nom de la famille
              </label>
              <input
                type="text"
                value={formData.nom || ''}
                onChange={(e) => setFormData({...formData, nom: e.target.value})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                placeholder="Ex: Canapé, Lit, Table..."
              />
            </div>
            <div className="flex justify-end gap-2">
              <button
                onClick={() => closeModal('famille')}
                className="px-4 py-2 text-gray-600 hover:text-gray-800 transition-colors"
              >
                Annuler
              </button>
              <button
                onClick={handleSaveFamille}
                className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
              >
                <Save className="w-4 h-4 inline mr-2" />
                Enregistrer
              </button>
            </div>
          </div>
        </Modal>

        {/* Modal Panne */}
        <Modal 
          isOpen={modals.panne} 
          onClose={() => closeModal('panne')}
          title={editingItem ? 'Modifier la panne' : 'Ajouter une panne'}
        >
          <div className="space-y-4">
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Nom de la panne
              </label>
              <input
                type="text"
                value={formData.nom || ''}
                onChange={(e) => setFormData({...formData, nom: e.target.value})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                placeholder="Ex: Pièce manquante, Bruit, Usure..."
              />
            </div>
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Familles concernées
              </label>
              <div className="space-y-2 max-h-40 overflow-y-auto">
                {famillesProduits.map(famille => (
                  <label key={famille.id} className="flex items-center">
                    <input
                      type="checkbox"
                      checked={(formData.familleIds || []).includes(famille.id)}
                      onChange={(e) => {
                        const currentIds = formData.familleIds || [];
                        if (e.target.checked) {
                          setFormData({...formData, familleIds: [...currentIds, famille.id]});
                        } else {
                          setFormData({...formData, familleIds: currentIds.filter(id => id !== famille.id)});
                        }
                      }}
                      className="mr-2"
                    />
                    {famille.nom}
                  </label>
                ))}
              </div>
            </div>
            <div className="flex justify-end gap-2">
              <button
                onClick={() => closeModal('panne')}
                className="px-4 py-2 text-gray-600 hover:text-gray-800 transition-colors"
              >
                Annuler
              </button>
              <button
                onClick={handleSavePanne}
                className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
              >
                <Save className="w-4 h-4 inline mr-2" />
                Enregistrer
              </button>
            </div>
          </div>
        </Modal>

        {/* Modal Sous-panne */}
        <Modal 
          isOpen={modals.sousPanne} 
          onClose={() => closeModal('sousPanne')}
          title={editingItem ? 'Modifier la sous-panne' : 'Ajouter une sous-panne'}
        >
          <div className="space-y-4">
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Nom de la sous-panne
              </label>
              <input
                type="text"
                value={formData.nom || ''}
                onChange={(e) => setFormData({...formData, nom: e.target.value})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                placeholder="Ex: Vis manquante, Grincement..."
              />
            </div>
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Panne parent
              </label>
              <select
                value={formData.panneId || ''}
                onChange={(e) => setFormData({...formData, panneId: parseInt(e.target.value)})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
              >
                <option value="">-- Sélectionnez une panne --</option>
                {typesPannes.map(panne => (
                  <option key={panne.id} value={panne.id}>
                    {panne.nom}
                  </option>
                ))}
              </select>
            </div>
            <div className="flex justify-end gap-2">
              <button
                onClick={() => closeModal('sousPanne')}
                className="px-4 py-2 text-gray-600 hover:text-gray-800 transition-colors"
              >
                Annuler
              </button>
              <button
                onClick={handleSaveSousPanne}
                className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
              >
                <Save className="w-4 h-4 inline mr-2" />
                Enregistrer
              </button>
            </div>
          </div>
        </Modal>

        {/* Modal Article */}
        <Modal 
          isOpen={modals.article} 
          onClose={() => closeModal('article')}
          title={editingItem ? 'Modifier l\'article' : 'Ajouter un article'}
        >
          <div className="space-y-4">
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Référence
              </label>
              <input
                type="text"
                value={formData.reference || ''}
                onChange={(e) => setFormData({...formData, reference: e.target.value})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                placeholder="Ex: CAP-001, LIT-002..."
              />
            </div>
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Nom
              </label>
              <input
                type="text"
                value={formData.nom || ''}
                onChange={(e) => setFormData({...formData, nom: e.target.value})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                placeholder="Ex: Canapé 3 places Lincoln..."
              />
            </div>
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Famille
              </label>
              <select
                value={formData.familleId || ''}
                onChange={(e) => setFormData({...formData, familleId: parseInt(e.target.value)})}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
              >
                <option value="">-- Sélectionnez une famille --</option>
                {famillesProduits.map(famille => (
                  <option key={famille.id} value={famille.id}>
                    {famille.nom}
                  </option>
                ))}
              </select>
            </div>
            <div className="flex justify-end gap-2">
              <button
                onClick={() => closeModal('article')}
                className="px-4 py-2 text-gray-600 hover:text-gray-800 transition-colors"
              >
                Annuler
              </button>
              <button
                onClick={handleSaveArticle}
                className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
              >
                <Save className="w-4 h-4 inline mr-2" />
                Enregistrer
              </button>
            </div>
          </div>
        </Modal>

        {/* Modal Message */}
        <Modal 
          isOpen={modals.message} 
          onClose={() => closeModal('message')}
          title={editingItem ? 'Modifier le message' : 'Ajouter un message'}
        >
          <div className="space-y-4">
            <div className="grid grid-cols-2 gap-4">
              <div>
                <label className="block text-sm font-medium text-gray-700 mb-2">
                  Famille (optionnel)
                </label>
                <select
                  value={formData.familleId || ''}
                  onChange={(e) => setFormData({...formData, familleId: e.target.value ? parseInt(e.target.value) : null})}
                  className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
                  <option value="">-- Aucune --</option>
                  {famillesProduits.map(famille => (
                    <option key={famille.id} value={famille.id}>
                      {famille.nom}
                    </option>
                  ))}
                </select>
              </div>
              <div>
                <label className="block text-sm font-medium text-gray-700 mb-2">
                  Panne (optionnel)
                </label>
                <select
                  value={formData.panneId || ''}
                  onChange={(e) => setFormData({...formData, panneId: e.target.value ? parseInt(e.target.value) : null})}
                  className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
                  <option value="">-- Aucune --</option>
                  {typesPannes.map(panne => (
                    <option key={panne.id} value={panne.id}>
                      {panne.nom}
                    </option>
                  ))}
                </select>
              </div>
            </div>
            <div className="grid grid-cols-2 gap-4">
              <div>
                <label className="block text-sm font-medium text-gray-700 mb-2">
                  Sous-panne (optionnel)
                </label>
                <select
                  value={formData.sousPanneId || ''}
                  onChange={(e) => setFormData({...formData, sousPanneId: e.target.value ? parseInt(e.target.value) : null})}
                  className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                  disabled={!formData.panneId}
                >
                  <option value="">-- Aucune --</option>
                  {sousPannes.filter(sp => sp.panneId === formData.panneId).map(sousPanne => (
                    <option key={sousPanne.id} value={sousPanne.id}>
                      {sousPanne.nom}
                    </option>
                  ))}
                </select>
              </div>
              <div>
                <label className="block text-sm font-medium text-gray-700 mb-2">
                  Article (optionnel)
                </label>
                <select
                  value={formData.articleId || ''}
                  onChange={(e) => setFormData({...formData, articleId: e.target.value ? parseInt(e.target.value) : null})}
                  className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
                  <option value="">-- Aucun --</option>
                  {articles.map(article => (
                    <option key={article.id} value={article.id}>
                      {article.reference} - {article.nom}
                    </option>
                  ))}
                </select>
              </div>
            </div>
            <div>
              <label className="block text-sm font-medium text-gray-700 mb-2">
                Contenu du message
              </label>
              <textarea
                value={formData.contenu || ''}
                onChange={(e) => setFormData({...formData, contenu: e.target.value})}
                rows={10}
                className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                placeholder="Saisissez le message type à envoyer au client..."
              />
            </div>
            <div className="flex justify-end gap-2">
              <button
                onClick={() => closeModal('message')}
                className="px-4 py-2 text-gray-600 hover:text-gray-800 transition-colors"
              >
                Annuler
              </button>
              <button
                onClick={handleSaveMessage}
                className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
              >
                <Save className="w-4 h-4 inline mr-2" />
                Enregistrer
              </button>
            </div>
          </div>
        </Modal>

        {/* Modal de confirmation de suppression */}
        <Modal 
          isOpen={modals.delete} 
          onClose={() => closeModal('delete')}
          title="Confirmer la suppression"
        >
          <div className="space-y-4">
            <div className="flex items-center gap-3 p-4 bg-red-50 rounded-lg">
              <AlertTriangle className="w-6 h-6 text-red-600 flex-shrink-0" />
              <div>
                <p className="font-medium text-red-800">Attention !</p>
                <p className="text-sm text-red-700">
                  Cette action est irréversible. Êtes-vous sûr de vouloir supprimer cet élément ?
                </p>
              </div>
            </div>
            {deleteTarget && (
              <div className="p-3 bg-gray-100 rounded-lg">
                <p className="font-medium">Élément à supprimer :</p>
                <p className="text-sm text-gray-600">
                  {deleteTarget.item.nom || deleteTarget.item.reference || 'Message'}
                </p>
              </div>
            )}
            <div className="flex justify-end gap-2">
              <button
                onClick={() => closeModal('delete')}
                className="px-4 py-2 text-gray-600 hover:text-gray-800 transition-colors"
              >
                Annuler
              </button>
              <button
                onClick={handleDelete}
                className="px-4 py-2 bg-red-500 text-white rounded-lg hover:bg-red-600 transition-colors"
              >
                <Trash2 className="w-4 h-4 inline mr-2" />
                Supprimer
              </button>
            </div>
          </div>
        </Modal>
      </div>
    </div>
  );
};

export default InterfaceSAV;
