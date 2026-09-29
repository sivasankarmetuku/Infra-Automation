import { useState, useEffect } from "react";

const defaultData = {
  spaces: [
    {
      id: 1,
      name: "Infrastructure",
      tasks: [
        {
          id: 101,
          title: "Patch Linux Servers",
          assignee: "Siva",
          priority: "High",
          status: "To Do"
        }
      ]
    }
  ]
};

const columns = ["Backlog", "To Do", "In Progress", "Review", "Done"];

export default function App() {
  const [data, setData] = useState(() => {
    const stored = localStorage.getItem("kanban-data");
    return stored ? JSON.parse(stored) : defaultData;
  });

  const [selectedSpace, setSelectedSpace] = useState(data.spaces[0].id);

  useEffect(() => {
    localStorage.setItem("kanban-data", JSON.stringify(data));
  }, [data]);

  const currentSpace = data.spaces.find(
    s => s.id === selectedSpace
  );

  const addTask = () => {
    const title = prompt("Task Name");
    if (!title) return;

    const task = {
      id: Date.now(),
      title,
      assignee: "",
      priority: "Medium",
      status: "Backlog"
    };

    const updated = data.spaces.map(space =>
      space.id === selectedSpace
        ? { ...space, tasks: [...space.tasks, task] }
        : space
    );

    setData({ ...data, spaces: updated });
  };

  const moveTask = (taskId, status) => {
    const updated = data.spaces.map(space => {
      if (space.id !== selectedSpace) return space;

      return {
        ...space,
        tasks: space.tasks.map(task =>
          task.id === taskId
            ? { ...task, status }
            : task
        )
      };
    });

    setData({ ...data, spaces: updated });
  };

  return (
    <div className="min-h-screen p-6 bg-gray-100">
      <div className="flex justify-between mb-5">
        <h1 className="text-3xl font-bold">
          Infra Automation Kanban
        </h1>

        <button
          onClick={addTask}
          className="bg-blue-600 text-white px-4 py-2 rounded"
        >
          New Task
        </button>
      </div>

      <div className="mb-5">
        <select
          value={selectedSpace}
          onChange={e =>
            setSelectedSpace(Number(e.target.value))
          }
          className="p-2 border rounded"
        >
          {data.spaces.map(space => (
            <option key={space.id} value={space.id}>
              {space.name}
            </option>
          ))}
        </select>
      </div>

      <div className="grid grid-cols-5 gap-4">
        {columns.map(column => (
          <div
            key={column}
            className="bg-white rounded-lg p-3 shadow"
          >
            <h2 className="font-bold mb-3">
              {column}
            </h2>

            {currentSpace.tasks
              .filter(t => t.status === column)
              .map(task => (
                <div
                  key={task.id}
                  className="bg-gray-50 border rounded p-3 mb-3"
                >
                  <h3 className="font-semibold">
                    {task.title}
                  </h3>

                  <div className="text-sm">
                    Assignee: {task.assignee || "Unassigned"}
                  </div>

                  <div className="text-sm">
                    Priority: {task.priority}
                  </div>

                  <select
                    value={task.status}
                    onChange={e =>
                      moveTask(task.id, e.target.value)
                    }
                    className="mt-2 border rounded p-1 w-full"
                  >
                    {columns.map(c => (
                      <option key={c}>{c}</option>
                    ))}
                  </select>
                </div>
              ))}
          </div>
        ))}
      </div>
    </div>
  );
}
