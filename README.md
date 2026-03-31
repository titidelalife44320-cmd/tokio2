import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gray-900 text-white p-6">
      {/* Header */}
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold">TOKIO TIKTOK</h1>
        <p className="text-gray-400 mt-2">Bienvenue sur mon site</p>
      </header>

      {/* About */}
      <section className="mb-10">
        <h2 className="text-2xl font-semibold mb-4">À propos de moi</h2>
        <Card className="bg-gray-800">
          <CardContent className="p-4">
            <p>
              Je suis un passionné de création de sites web. J'aime le design,
              le développement et créer des expériences modernes.
            </p>
          </CardContent>
        </Card>
      </section>

      {/* Projects */}
      <section className="mb-10">
        <h2 className="text-2xl font-semibold mb-4">Mes projets</h2>
        <div className="grid md:grid-cols-3 gap-4">
          {["Projet 1", "Projet 2", "Projet 3"].map((project, i) => (
            <motion.div
              key={i}
              whileHover={{ scale: 1.05 }}
            >
              <Card className="bg-gray-800">
                <CardContent className="p-4">
                  <h3 className="text-xl font-bold">{project}</h3>
                  <p className="text-gray-400 mt-2">
                    Description rapide du projet.
                  </p>
                </CardContent>
              </Card>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section className="text-center">
        <h2 className="text-2xl font-semibold mb-4">Contact</h2>
        <Button>Me contacter</Button>
      </section>
    </div>
  );
}
